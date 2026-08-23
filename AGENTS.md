# CharityGraph Viewer — Agent Instructions

**Status:** Canonical repository instructions  
**Version:** 0.2

## Shared CharityGraph project memory

The canonical shared state and planning documents live in the sibling
[`charitygraph-data`](https://github.com/gregorycwhill/charitygraph-data) repository:

- `DOCUMENT_AUTHORITY.md`
- `CURRENT_STATE.md`
- `ROADMAP.md`
- `IMPLEMENTATION_PLAN.md`
- `TEST_PLAN.md`
- `CODEX_TO_CHATGPT_HANDOFF.md`

Read those documents before changing cross-product contracts. Do not create or maintain workspace-root duplicates.

## Product boundary

CharityGraph Viewer provides discovery, search, inspection, provenance and correction over an explicitly selected CharityGraph Data release.

Do not add personalised recommendations, charity quality scores, best-charity rankings, donation nudges, portfolio optimisation, payments, user-account infrastructure or an independent Viewer datastore.

Viewer is not an independent source of truth. It must not manually maintain charity facts, summaries, taxonomies, embeddings or estimates. Cards are public release projections; Builder’s private working records remain outside Viewer.

## Identity and release fidelity

Use the CharityGraph subject and stable public card route for navigation. A legacy subject ID may be displayed or searched when required by public contract 0.5 compatibility; it is not a new internal identity. ABN and ACNC identifiers remain external identifiers.

Viewer renders the selected public card projection and must not rewrite substantive card content client-side. Display provenance, confidence, estimation method, release and freshness context clearly.

## Static-first operation

Prefer the static browser architecture. Do not introduce a backend unless a concrete requirement cannot reasonably be met by static/public data and external contribution mechanisms.

## Search versus recommendation

Allowed:

- text, facet and taxonomy search;
- descriptive semantic search and semantic neighbours;
- multi-entity centroid/blend exploration;
- factual side-by-side comparison;
- transparent retrieval sorting.

Not allowed:

- unexplained desirability ranking;
- “recommended for you” or “better charities” language;
- quality stars or scores;
- hidden objectives intended to change giving behaviour.

Search ranking must be understandable as retrieval relevance, not charity merit. Similarity is descriptive.

## Corrections

- Field-level controls create correction proposals; they do not mutate source data.
- Prefill the subject context, field, current value and release/version where available.
- Correction status/history is inspectable only where a governed public projection exists.
- Open-ended discussion is distinct from structured correction.
- Never publish raw submissions automatically.

## Accessibility and completion

Primary controls, cards and correction actions must be keyboard- and screen-reader-usable. Mobile must remain usable. Before declaring work complete, run tests, inspect representative fixtures, verify deep links, correction prefill, provenance and estimation visibility, and confirm no recommendation language or logic has slipped in.