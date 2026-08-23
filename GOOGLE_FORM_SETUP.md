# CharityGraph correction and feedback-form operations

**Status:** Current repository guide for the external correction/feedback intake  
**Scope:** Viewer prefill wiring only; the external form remains separately owned

The Viewer’s current `src/corrections.mjs` contains the verified prefill endpoint and the code-level entry mapping. This repository does not rename or configure the external form remotely, and this guide makes no claim about the form’s external title or ownership.

## Human-facing fields

| Field | Purpose |
| --- | --- |
| Feedback type | Factual correction, outdated/missing information, self-description, classification/methodology dispute or general feedback |
| Organisation / display name | Optional display context |
| Legacy subject ID | Human-readable label for the public 0.5 identity; current code maps the exact `causebase_id` field |
| Dataset / release version | Release challenged |
| Viewer / card URL | Prefilled public route where available |
| Field / section | Field-level challenge context |
| Current displayed value | Optional snapshot, subject to the 1,200-character URL safeguard |
| Proposed correction or feedback | Required contributor explanation |
| Explanation | Why the change is warranted |
| Supporting source/evidence URL | Public evidence preferred; confidential documents are not requested |
| Contact name/email | Optional follow-up only |

The current source mapping uses the existing organisation, exact legacy `causebase_id`, dataset version, Viewer URL, field and current-value entries. Do not rename the compatibility field or invent `charitygraph_id`.

## Operational privacy rules

The form is a convenience intake, not the correction data model. Do not publish responses, contact details, supporting material or an unmoderated proposal ledger. Viewer only creates a prefilled handoff; Builder moderation and governed decisions determine whether a correction enters a later release.

Keep the endpoint and entry mapping aligned with `src/corrections.mjs`, and verify any external-form change with the form owner before changing code. The module-owned endpoint is not configured through a global window variable.