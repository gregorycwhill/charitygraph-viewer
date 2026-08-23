# CharityGraph Viewer Correction Flow

**Status:** Canonical Viewer correction-flow contract  
**Version:** 0.2

## 1. Purpose

Make it easy for a person who spots a problem to challenge a specific CharityGraph assertion without giving direct edit access to generated data.

## 2. Field-level interaction

Where appropriate, a field or section exposes **Suggest correction**. The action carries the available context automatically:

- legacy subject ID, represented in the public 0.5 payload by the exact compatibility field `causebase_id`;
- organisation/display name;
- field or assertion;
- current value;
- Data release version;
- Viewer URL.

The contributor supplies what is wrong or missing, a proposed correction where appropriate, the reason and supporting public evidence.

## 3. Correction versus self-description

Distinguish factual, stale, missing or classification corrections from attributed organisation-authored self-description. A self-description update does not replace CharityGraph’s neutral synthesis.

## 4. Proposal lifecycle

A correction follows the governed workflow:

`Lodged → Under review → Queried → Accepted/Rejected → Incorporated`

The Viewer may show a pending **Correction proposed** state only when a governed public status projection exists. Accepted changes appear in a later validated release; rejected history is shown only where policy permits.

Discussion is a separate action and does not alter a card.

## 5. Current intake integration

The current implementation in `src/corrections.mjs` owns the external Google Forms prefill endpoint and exports `correctionUrl(entity, field, currentValue, viewerUrl)`. The endpoint is module-owned; no global-window endpoint configuration is used.

The endpoint receives the existing code-level mapping for organisation, exact legacy `causebase_id`, dataset version, Viewer URL, field and current value. The field mapping is an implementation detail and must remain aligned with `src/corrections.mjs`; do not rename the compatibility field to `charitygraph_id`.

`current_value` is included only when its string length is at most `MAX_PREFILL_VALUE_LENGTH` (currently 1,200). Longer values are blanked while subject, release, field and Viewer URL context remain available.

The external form is a convenience intake, not the identity or governance contract. It must not publish raw submissions, contact details, supporting material or an unmoderated proposal ledger. The Builder proposal/decision workflow remains authoritative.

## 6. Privacy and framing

Use neutral language: CharityGraph is built from public evidence and may be incomplete or wrong; contributors can explain what should change and why. Do not imply infallibility or a right to veto supported neutral description. Do not expose private responses, credentials or additional form information.

Promotional rewrites should be redirected to a specific factual issue or attributed self-description update.