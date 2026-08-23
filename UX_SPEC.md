# CharityGraph Viewer UX Specification

**Status:** Canonical Viewer experience contract  
**Version:** 0.2

## 1. Purpose

CharityGraph Viewer helps people inspect the CharityGraph information space through a public card projection.

The primary loop is:

**Discover → Search → Inspect → Verify → Correct**

Semantic exploration extends discovery, but Viewer does not recommend or persuade.

## 2. Search and exploration

Support name, ABN/identifier, keyword, geography, taxonomy, activity, beneficiary, participation and appropriate financial/size filters. Retrieval ranking represents relevance, not merit.

Semantic search may retrieve organisations near a descriptive natural-language query. Semantic neighbours use neutral labels such as **Similar organisations** or **Semantic neighbours**. A multi-select blend must explain that it finds semantic proximity to the selected set, not preference or quality.

## 3. Card layout and sections

A desktop layout separates search/results from the selected CharityGraph card. The card may include:

- identity, names, status, website and external identifiers;
- a neutral CharityGraph summary;
- clearly attributed organisation self-description;
- activities, beneficiaries and role-specific geography;
- stable participation modes and current opportunities with freshness;
- financial facts, metrics and estimates with method/confidence/provenance;
- multiple taxonomy views;
- evidence, citations, observation dates and derivation information;
- descriptive semantic relationships;
- correction/discussion status where available.

Viewer renders the selected CharityGraph Data release and must not invent facts or recompute release fields differently in JavaScript.

## 4. Navigation and correction

Each public card has a stable addressable route. Selecting a result updates the URL and a shared link restores the selected card. Challengable fields expose a correction action with subject, field, current value and release context prefilled where possible. The action creates a proposal, not an immediate edit.

Show lodged, under-review, queried, accepted, rejected and incorporated statuses only when governed data exists. Discussion and correction remain separate actions.

## 5. Descriptive data views

A dense grid/table may be provided as a secondary representation for data-oriented users, with filtering, sorting, column selection and export. It must not become a recommendation surface.

Do not introduce **Top picks**, **Best match**, **Recommended for you**, **Give now**, quality stars or desirability scores. Downstream applications may construct those experiences from CharityGraph Data.

## 6. Accessibility, responsive behaviour and tone

The two-pane desktop design degrades to sequential mobile views. Core actions do not depend on hover; keyboard access and screen-reader semantics are required. Viewer should feel like public data infrastructure and an inspection tool, not a fundraising campaign.