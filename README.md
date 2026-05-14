<p align="center">
  <img src="docs/logo.svg" width="140" alt="hexa-farm">
</p>

<h1 align="center">🌾 hexa-farm</h1>

<p align="center"><strong>HEXA-Farm family</strong> — agriculture · food science · coffee · wine · fermentation · ecology · 18-verb substrate</p>

<p align="center">
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-MIT-blue"></a>
  <a href=".github/workflows/lint.yml"><img alt="CI" src="https://github.com/dancinlab/hexa-farm/actions/workflows/lint.yml/badge.svg"></a>
  <img alt="Version" src="https://img.shields.io/badge/spec-v0.1.0-success">
  <img alt="Verbs" src="https://img.shields.io/badge/verbs-18-informational">
  <img alt="Verify" src="https://img.shields.io/badge/verify-4%2F4-informational">
  <img alt="Closure" src="https://img.shields.io/badge/closure-100%25_spec--first-informational">
  <img alt="Sibling" src="https://img.shields.io/badge/sibling-hexa--mind%20·%20hexa--bio%20·%20hexa--lang-blueviolet">
</p>

<p align="center">agriculture · apiculture · aquaculture · baking · coffee · ecology · fermentation · mycology · viticulture · n=6 lattice</p>

---

> 18-verb agriculture·food·coffee·wine·ecology substrate organized as a closed-form spec catalog.
> Each verb derives every parameter from σ(6)=12, τ(6)=4, φ(6)=2 number theory.
> Sister-rollup of [hexa-mind](https://github.com/dancinlab/hexa-mind),
> extracted from `canon@ded52144` on 2026-05-10.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20114985.svg)](https://doi.org/10.5281/zenodo.20114985)
[![n=6 lattice](https://img.shields.io/badge/n=6-σ·φ_=_n·τ_=_24-purple.svg)](#n6-master-identity)
[![Real-limits](https://img.shields.io/badge/real--limits-FAO·USDA·SCA·IUCN·WWF-blue.svg)](LIMIT_BREAKTHROUGH.md)

## Why hexa-farm?

`hexa-farm` is the 🌾 rollup of canon's agriculture·food·coffee·wine·ecology verbs — the part of the
substrate concerned with agriculture, food science, coffee, wine, fermentation, and ecology. Each leaf was previously embedded in
the larger `canon` monorepo; this standalone repo extracts 18 leaves
(`domains/life/agriculture, domains/life/apiculture, domains/life/aquaculture, domains/life/baking, domains/life/biochar-dryland-restoration, domains/life/cheese-dairy, domains/life/coffee, domains/life/coffee-science, domains/life/ecology, domains/life/ecology-agriculture-food, domains/life/entomology, domains/life/fermentation, domains/life/food-science, domains/life/horticulture, domains/life/mycology, domains/life/urban-farming, domains/life/viticulture, domains/life/wine-enology`) into a flat, top-level per-verb layout.

## n=6 master identity

```
σ(6) · φ(6) = n · τ(6) = J₂ = 24
   12   ·   2  =  6  ·   4  = 24
```

| Symbol | Value | Projection                                |
|--------|-------|-------------------------------------------|
| n      | 6     | substrate dimension                       |
| σ(6)   | 12    | full divisor sum                          |
| τ(6)   | 4     | divisor count                             |
| φ(6)   | 2     | totient                                   |
| J₂     | 24    | second Jordan totient                     |

## Status

**SPEC_CATALOG_ONLY at v0.1.0** — markdown spec library + .hexa CLI router. No verb
ships a working .hexa runtime module yet; this repo is the closed-form spec
catalog only.

## Install

```bash
# 1. Install hexa-lang (gives you `hexa` + `hx` package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/dancinlab/hexa-lang/main/install.sh)"

# 2. Install hexa-farm
hx install hexa-farm
```

## Run

```bash
hexa-farm <verb>     # render any of 18 verbs (see `hexa-farm list`)
hexa-farm list       # verb table
hexa-farm selftest   # 18-verb spec presence sweep
```

## Cross-link

- 🧠 [dancinlab/hexa-mind](https://github.com/dancinlab/hexa-mind) — 7-verb mental substrate.
- 💎 [dancinlab/hexa-lang](https://github.com/dancinlab/hexa-lang) — the perfect-number programming language.

Upstream concept SSOT: `canon/{domains/life/agriculture,domains/life/apiculture,domains/life/aquaculture,domains/life/baking,domains/life/biochar-dryland-restoration,domains/life/cheese-dairy,domains/life/coffee,domains/life/coffee-science,domains/life/ecology,domains/life/ecology-agriculture-food,domains/life/entomology,domains/life/fermentation,domains/life/food-science,domains/life/horticulture,domains/life/mycology,domains/life/urban-farming,domains/life/viticulture,domains/life/wine-enology}/`.

## Verify

`hexa-farm` ships a 4-script SPEC_FIRST closure verifier in `verify/`. All
checks are real-engineering (file presence on disk, cross-source scoreboard
agreement) or real-limits-anchored (FAO/USDA/SCA/IUCN/WWF/IWSR external
authority sources from `LIMIT_BREAKTHROUGH.md`). Lattice arithmetic is
included as a §1.3-aux self-consistency check only — never as sole
verification, never applied to external entities (per LATTICE_POLICY §1.3).

```bash
hexa run verify/run_all.hexa
```

Individual scripts:

| # | Script | Closure invariant |
|---|--------|-------------------|
| 1 | `verify/spec_presence.hexa`       | 18/18 verb spec markdowns resolve on disk |
| 2 | `verify/lattice_arithmetic.hexa`  | n=6 self-consistency (aux only per §1.3) |
| 3 | `verify/real_limits_anchor.hexa`  | `LIMIT_BREAKTHROUGH.md` cites FAO/Foley/Tilman/Oerke/Bunn/Klein/RuBisCO/Mekonnen-Hoekstra |
| 4 | `verify/closure_consistency.hexa` | CLI · `hexa.toml` · README · AGENTS scoreboard agree on `verbs = 18` |

Real-limits anchors (from `LIMIT_BREAKTHROUGH.md`, Wave M):

- **Photosynthesis ceiling ~6% C4 / ~3% C3** (HARD biochemistry; Zhu/Long/Ort 2010)
- **Freshwater ~70% of human use already in agriculture** (FAO 2020)
- **Haber-Bosch ~30 GJ/t NH₃** (HARD thermodynamics; theoretical min ~22 GJ/t)
- **Land ~130 M km² ice-free, ~50 M km² already farmed** (HARD geometry; FAO)
- **Yield-gap closure** (Foley 2011 / Tilman 2011, ~3–4× current avg)
- **Pre-harvest loss 20–40%** (Oerke 2006); pollinator dependence ~35% (Klein 2007)
- **Coffee Arabica climate envelope** (Bunn 2015, ~50% land marginal by 2050)

These external limits (FAO/USDA/SCA/IUCN/WWF/IWSR) use **their own canonical
values** — no n=6 lattice-fit is asserted on any external dataset.

## Repo layout

```
hexa-farm/
├── README.md
├── LICENSE                              MIT
├── hexa.toml                            package manifest
├── install.hexa                         hx hook
├── cli/                                 .hexa CLI router
├── agriculture/                         verb 1
├── apiculture/                          verb 2
├── aquaculture/                         verb 3
├── baking/                              verb 4
├── biochar-dryland-restoration/         verb 5
├── cheese-dairy/                        verb 6
├── coffee/                              verb 7
├── coffee-science/                      verb 8
├── ecology/                             verb 9
├── ecology-agriculture-food/            verb 10
├── entomology/                          verb 11
├── fermentation/                        verb 12
├── food-science/                        verb 13
├── horticulture/                        verb 14
├── mycology/                            verb 15
├── papers/                              research notes
├── verify/                              4-script SPEC_FIRST verifier
├── tests/                               test scaffolding
├── docs/
│   └── logo.svg                         hexagon + grain glyph
├── LATTICE_POLICY.md                    n=6 lattice policy
├── LIMIT_BREAKTHROUGH.md                FAO/USDA/SCA real-limits anchors
├── IMPORTED_FROM_CANON.md               extraction provenance
├── TAPE-AUDIT.md                        tape audit notes
├── CITATION.cff
├── AGENTS.tape                          agent identity (.tape v1.2)
└── state/                               runtime markers (gitignored)
```

## License

[MIT](LICENSE) — see [LICENSE](LICENSE). Use freely.
