---
title: "Exchange rates and monetary policy with heterogeneous agents: Sizing up the real income channel — Ballpark Entry"
schema_type: ScholarlyArticle
about:
  doi: 10.3386/w28872
  authors: [Auclert, Rognlie, Souchier, Straub]
  year: 2024
  publication: "NBER Working Paper 28872 (also SSRN 3856853)"
keywords: [HANK, open-economy, real-income-channel, exchange-rate, intertemporal-MPC, sequence-space-Jacobian]
econ_ark_topic:
  - HANK
  - open-economy
  - sequence-space-Jacobian
jel: [E12, E52, F31, F41]
difficulty: stretch
tier: formalized
has_formalization_layer: true
# Scope of the formalization layer in this directory.
# Canonical record: bellman-excerpt.md §13 ("Open items").
# Same scope statement appears in AGENTS.md (top callout) and
# OpenHA_summary.ipynb (Pointer-to-formalization-layer cell).
formalization_scope: household-and-aggregate
formalization_scope_note: |
  dolo-plus-draft.yaml encodes the household three-stage period
  (shocks -> cons -> disc) of bellman-excerpt.md §8. As of the
  June 2026 follow-up PR, aggregate-draft.yaml encodes the
  aggregate / GE closure (CPI, real exchange rate, real UIP,
  RoW demand, sticky-wages Phillips curve, monetary rule, NFA,
  current account) -- the 16-equation system E.1-E.16 of
  bellman-excerpt.md §7, grouped into six blocks -- and
  openha-ge-draft.yaml wires the household and aggregate blocks
  into a general-equilibrium composition. The aggregate-block
  container syntax is SPECULATIVE (dolo-plus has no canonical
  aggregate sequence-space idiom); the canonical record of the
  scope history and the syntax workaround is bellman-excerpt.md
  §13.1 and §13.5. The aggregate YAML is the Cursor/Claude
  Extract draft; the Matsya evaluate pass on it is the remaining
  human-in-the-loop step (see AGENTS.md "Common next tasks").
formalization_horizon: infinite-stationary
requires: [CRRA, EGM, Markov-chain-shocks, Rouwenhorst, sequence-space-Jacobian]
ballpark_contributor:
  name: "Junhyeok (Julian) Shin"
  date: 2023-05-06
updated_by:
  - name: "Siying Li"
    date: 2025-02-13
  - name: "Siying Li"
    date: 2026-04-23
    note: "formalize-and-finalize for Topics 180.606 assignment #140 (Claude Opus 4.7 review): perch-ready household Bellman; bellman-excerpt.md / dolo-plus-draft.yaml / verification.md / matsya-session.txt / AGENTS.md committed; prior-literature trimmed to 6 anchors with iMPC anchor added; intro pitch added; round-8 Matsya YAML iteration."
  - name: "Siying Li"
    date: 2026-05-09
    note: "round-9 instructor-review revisions (PR #73 review): household-only YAML scope made explicit and consistent across bellman-excerpt §13 / AGENTS.md / this frontmatter / summary notebook; tail Open-items block migrated to inline `# unresolved:` comments at point of divergence per CONTRIBUTING.md line 44; horizon: infinite-stationary declared at YAML preamble; asset layer added (OpenHA-perch-graphs.md mermaid diagrams + bellman-excerpt.pdf); upstream master merge (rename index.md -> OpenHA.md per PR #90, README.md per PR #81, root myst.yml registration per PR #87)."
  - name: "Siying Li"
    date: 2026-06-02
    note: "follow-up PR (the aggregate-block step from the bellman-excerpt §13.1 blueprint): added aggregate-draft.yaml encoding the GE closure E.1-E.16 (§7) in six blocks, and openha-ge-draft.yaml wiring household + aggregate into a GE composition; scope advanced from household-block-only to household-and-aggregate; canonical syntax-workaround record added as bellman-excerpt §13.5; verification.md Round 10 (accept/edit/reject for the Extract draft); AGENTS.md status + next-tasks updated. Matsya evaluate pass on the aggregate block recorded as the remaining open item."
---

```{include} OpenHA_intro.ipynb
```

```{include} OpenHA_prior-literature.ipynb
```

```{include} OpenHA_summary.ipynb
```

```{include} OpenHA_subsequent-literature.ipynb
```
