# Engineering decisions

## 1. Preserve intent before crossing a system boundary

**Problem:** an operator needs the customer's selected product and request context even if the catalog later changes or delivery fails.

**Implementation:** WordPress inquiry snapshots, product/source fields, a durable outbox, signed delivery, and atomic CRM intake. CRM intake compares a request identity and payload hash before creating records.

**Trade-off:** delivery is eventually consistent. A queue needs visible failures and recovery; WP-Cron depends on traffic. Local persistence and queue insertion are separate operations, so monitoring must detect requests that have not been queued as well as failed queue entries. Idempotency prevents repeat creation for the same request identity, not all semantically similar customer submissions.

## 2. Make follow-up a task, not a second status field

**Problem:** a deal status says where work stands but does not say who should act next or when.

**Implementation:** the workspace chooses the earliest open, non-deleted task. Database triggers mirror that task into legacy deal follow-up fields; date ordering is stabilized by creation time and ID. Today groups work around actionable conditions.

**Trade-off:** compatibility is easier for old views, but the derived fields must not become an independent scheduling system. A completed task does not imply completed delivery, installation, or payment.

## 3. Treat issuance as a commitment

**Problem:** multiple staff can edit a quote, while changing tax settings or retrying a request can invalidate a naive browser-only calculation.

**Implementation:** draft revisions, expected versions/settings timestamps, guarded atomic issuance, and request receipts. Money uses integer agorot and explicit tax modes; issued quote versions are preserved.

**Trade-off:** conflicts require refresh and review. Staff must explicitly approve prices and issue a version. The screenshot deliberately leaves the approved-price input empty rather than inventing a catalog price. Stable sharing exists in source, but public sharing and signing require separate hosted verification.

## 4. Enforce the boundary on the server

**Problem:** a static frontend cannot keep privileged credentials secret or reliably enforce company access.

**Implementation:** staff authentication, company-scoped RLS, role checks in SQL workflows, and server-side Edge Functions for privileged intake and external operations. Public quote output is allowlisted rather than exposing CRM tables anonymously.

**Trade-off:** correctness depends on database policies, function grants, secret configuration and role testing together. Local UI fixtures validate presentation, not authentication security. This case study makes no security-certification claim.
