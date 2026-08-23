# CharityGraph Viewer Development

Viewer is intentionally dependency-light and consumes explicit CharityGraph Data release projections.

## Run tests

```powershell
npm test
```

## Run locally

From the Viewer repository:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`.

The checked-in `public/data/` directory in this bootstrap package contains only synthetic fixture output so the Viewer runs immediately. In the real local workspace, replace or sync fixture assets from a validated CharityGraph Data publication staging directory or published release. Viewer must never read Builder’s raw or processed working directories.

## Current vertical-slice capabilities

Implemented:

- keyword search across the fixture corpus;
- result index and selected CharityGraph card projection;
- CharityGraph summary versus attributed organisation self-description;
- fundraising estimate method/confidence;
- multi-taxonomy display;
- evidence display;
- fixture-only precomputed neighbours, not public semantic functionality;
- deep links via entity hash;
- field-level correction context handoff.

Deliberately not implemented yet:

- live correction submission;
- GitHub Discussions integration;
- faceted filters;
- real semantic query embedding;
- multi-select semantic blend;
- grid library;
- map;
- recommendation logic;
- any backend.

The current fixture schema is provisional. A public enriched-card release requires real embeddings where semantic features are shown and a private, prefilled correction-intake handoff with traceable acknowledgement.