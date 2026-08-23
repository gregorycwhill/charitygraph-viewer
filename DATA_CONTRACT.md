# CharityGraph Viewer Data Contract

**Status:** Viewer implementation boundary for the implemented public contract 0.5  
**Version:** 0.5 compatibility

## 1. Authority and boundary

CharityGraph Viewer consumes the implemented public contract 0.5 published by CharityGraph Data. It reads validated published or explicitly staged release projections and never Builder’s private source or processed working directories.

Viewer is a convenience interface over an independently usable public Data product. It does not maintain an independent charity datastore or author a new public contract.

The public 0.5 payload retains the exact legacy compatibility field `causebase_id`. In human-facing prose this is the **legacy subject ID**. Do not replace it with `charitygraph_id`. Builder’s future internal identity is `subject_id`; that internal term does not change the immutable public 0.5 contract.

## 2. Required public capabilities

Viewer needs published data sufficient to list/index subjects, search/filter, load a selected public card projection, display provenance and estimation methods, inspect taxonomies, display correction status and navigate descriptive semantic similarity where enabled.

## 3. Release projections

CharityGraph Data may publish a browser index, per-subject JSON, Markdown cards, taxonomy artefacts, correction status projections, semantic indexes and analytical CSV/JSONL/Parquet assets. Exact file layout is release-owned.

A browser index may include legacy subject ID, subject kind, names, external identifiers, geography, source-aware coverage, taxonomy facets, participation flags, selected financial/size fields and a stable card locator. The legacy subject ID is not the Viewer’s new internal identity.

A selected public card projection carries the release-safe identity, observations, source references, compact evidence, coverage, derivatives and release metadata allowed by contract 0.5. Viewer representations must agree on shared released values.

## 4. Representation and semantic authority

If Viewer displays a field, the published CharityGraph card projection is authoritative for that release. Viewer must not recompute financial metrics, taxonomy assignments or prose differently, except for explicitly Viewer-only descriptive exploration such as semantic blending.

Compact semantic indexes are derived release assets and must identify their method/version. Failure of a secondary index must not prevent basic search and card inspection where possible.

## 5. Version, freshness and failure behaviour

Viewer displays or determines the Data release/version, relevant card/schema version and publication time. It distinguishes not-found-after-assessment, source unavailability, retrieval failure and not-yet-processed work, and does not present stale retained observations as current without indication.

Correction proposals identify the release and value challenged. Source links and downloadable Data artefacts remain available without requiring the national corpus for ordinary browsing.

## 6. Agent usability and future contracts

Published data provides stable subject/card routes, per-subject JSON and Markdown, machine-readable release/licence/schema metadata, provenance and freshness conventions, release discovery and selective retrieval.

Any future public-contract change requires a separate product decision, versioned schemas/examples, migration and losslessness analysis, coordinated Data/Viewer acceptance and a new immutable release. This document does not propose or implement one.