# Verification and scope

Review date: **7 November 2026**. This document separates source evidence, current local checks and historical production observations.

## Evidence matrix

| Capability | Evidence | Boundary |
| --- | --- | --- |
| Door/handle visualization | Current live public builder selection and original-versus-preview comparison | Selection only; no compatibility certification or inquiry submission |
| AI-assisted visual preparation | Inspected image-generation pilot and layered-asset provenance records | Approximate visual prototypes; no real-time model call or physical-fit certification |
| WhatsApp handoff | Inspected formatter and post-save browser navigation; current real landing-page preview with fictional text | No message sent; no production save or delivery tested |
| Catalog and product inquiry screen | Current live browser reads; WordPress site-info read succeeded | No form submitted |
| WordPress persistence and outbox | Inspected public/product intake handlers and outbox PHP source | Current live delivery not exercised |
| Signed, idempotent CRM intake | Inspected intake Edge Function and atomic intake migration | Signature configuration and live synchronization not revalidated |
| Task-first Today and work item | Current local real frontend with fictional HTTP fixtures; workspace regression script passed | Backend auth, persistence and production writes not exercised by screenshots |
| Quote preparation and totals | Actual composer; workspace and quote-document regression scripts passed | Screenshot is an unsaved draft, with no invented approved price |
| Revision/issuance safeguards | Inspected workspace SQL migration | No quote issued in production |
| Mobile work item | Actual frontend at 390 × 844; no horizontal overflow in captured state | Not a complete responsive or accessibility audit |
| Analytics/date logic | Existing business-analytics and daily-workspace scripts passed locally | No business figures published; no accounting reconciliation claim |
| CRM release | 1 November 2026 project handover records merged release, applied migration, rollback-only database tests and live read-only inspection | Historical evidence, not current end-to-end certification |
| Sharing/signing and outbound delivery | Source and prior release notes only | Current public-link, signing and provider delivery remain unverified |

## Screenshot provenance

Original captures were taken on 6 November 2026; the door-and-handle CRM and WhatsApp additions were captured on 7 November 2026. Original desktop exports are 1440 × 1000, mobile 390 × 844; browser-backed builder and additional captures use the available content viewport, with a focused crop for the WhatsApp landing panel. WebP images are flattened exports without EXIF/XMP metadata. The overview is a composition of two of these captures, not a new interface.

| File | Environment and action |
| --- | --- |
| `01-website-catalog.webp` | Live public catalog; transient chat popup closed using its own control |
| `02-product-inquiry.webp` | Live public product page, scrolled to empty inquiry fields; no submission |
| `03-crm-today.webp` | Actual local CRM code, fictional customer/task fixture |
| `04-customer-context.webp` | Same fictional work item opened through the application |
| `05-quote-workflow.webp` | Actual quote composer opened from that work item; no issuance or save |
| `06-mobile-experience.webp` | Same work item at mobile width |
| `07-door-builder.webp` | Live public builder opened directly from its product-page embedded frame; original black 8020 door compared with pull handle 190 visualization; no submission |
| `08-handle-selection.webp` | Same live builder with its real handle list open and pull handle 190 selected; no submission |

CRM requests were confined to loopback fixtures; external requests were blocked. No production configuration file was served. Fictional records are explicitly labeled in Hebrew. The website form was never submitted, and the CRM fixture was seeded independently. The captures therefore illustrate a coherent product scenario, not a measured synchronization event. No UI redesign was performed for the captures. A public business contact visible in the website header is existing public site content, not customer information.

| Additional file | Environment and action |
| --- | --- |
| `09-customer-door-and-handle.webp` | Actual local CRM with a separately seeded fictional combined door/handle inquiry, 7 November |
| `10-crm-selected-products.webp` | Same fictional configuration in the actual products/quote tab, 7 November |
| `11-whatsapp-draft.webp` | Focused real WhatsApp landing panel with independently prepared fictional text, 7 November; no send action |

The three additions use an explicit local-only backend configuration and a CSP restricting API connections to the local server. A real public product image is used in the fictional CRM case. The fictional message is independently prepared from the inspected formatter's field order and published as text; it is not a captured real customer message.

## Contribution evidence

The project requirements, UX audit and release handovers document user-directed workflow priorities, implementation approval, staged validation and release decisions. Source inspection supports the mechanisms described here. This supports the stated role of requirements/workflow ownership and implementation direction; it does not establish exclusive authorship of all code, the original website, brand, or manufacturer assets. AI coding assistance was part of implementation and investigation. Asset provenance also documents AI-assisted early visual prototypes. The inspected live renderer composes prepared layers; no per-selection model call is demonstrated.

## What remains

- Exercise a new fictional inquiry through a dedicated hosted staging environment, including outbox retry/replay and CRM read-back.
- Validate current roles and company boundaries using separate staging accounts.
- Verify quote draft conflicts, issuance retries, public sharing and signing in hosted staging.
- Resolve the previously reported mobile website chat/form obstruction across templates and scroll states.
- Verify provider delivery, integration freshness and accounting/POS reconciliation separately.
- Establish a baseline before reporting response-time, throughput or commercial improvement.

## Public repository boundaries

This repository includes documentation, diagrams, reviewed flattened screenshots and one explicitly fictional message text. It excludes original source code, database exports, private release documents, private project identifiers, runtime configuration, logs, access instructions and production history. Code extracts and a runnable demo were omitted because source disclosure rights are not established by repository access alone.

The destination account is **Jossefo**, verified through the connected GitHub profile. On 6 November 2026, the project owner confirmed permission for public portfolio use of the brand, interface screenshots and product/manufacturer imagery included here. This approval covers this reviewed case-study collection; it does not establish a general license to third-party assets or authorize release of the underlying source code.
