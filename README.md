# 🌾 hexa-farm — n=6 agriculture, food science, coffee, wine, fermentation, and ecology substrate (18-verb library)

> 18-verb agriculture·food·coffee·wine·ecology substrate organized as a closed-form spec catalog.
> Each verb derives every parameter from σ(6)=12, τ(6)=4, φ(6)=2 number theory.
> Sister-rollup of [hexa-mind](https://github.com/dancinlab/hexa-mind),
> extracted from `canon@ded52144` on 2026-05-10.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20114985.svg)](https://doi.org/10.5281/zenodo.20114985)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.1.0-informational.svg)](hexa.toml)
[![Verbs: 18](https://img.shields.io/badge/verbs-18-blue.svg)](#verbs)
[![n=6 lattice](https://img.shields.io/badge/n=6-σ·φ_=_n·τ_=_24-blue.svg)](#n6-master-identity)
[![Verify: 4/4 PASS](https://img.shields.io/badge/verify-4%2F4_PASS-brightgreen.svg)](#verify)
[![Closure: 100%](https://img.shields.io/badge/closure-100%25_spec--first-brightgreen.svg)](#verify)
[![Real-limits](https://img.shields.io/badge/real--limits-FAO·USDA·SCA·IUCN·WWF-blue.svg)](LIMIT_BREAKTHROUGH.md)

---

## Why hexa-farm?

`hexa-farm` is the 🌾 rollup of canon's agriculture·food·coffee·wine·ecology verbs — the part of the
substrate concerned with agriculture, food science, coffee, wine, fermentation, and ecology. Each leaf was previously embedded in
the larger `canon` monorepo; this standalone repo extracts 18 leaves
(`domains/life/agriculture, domains/life/apiculture, domains/life/aquaculture, domains/life/baking, domains/life/biochar-dryland-restoration, domains/life/cheese-dairy, domains/life/coffee, domains/life/coffee-science, domains/life/ecology, domains/life/ecology-agriculture-food, domains/life/entomology, domains/life/fermentation, domains/life/food-science, domains/life/horticulture, domains/life/mycology, domains/life/urban-farming, domains/life/viticulture, domains/life/wine-enology`) into a flat, top-level per-verb layout.

---

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

---

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

---

## Cross-link

- 🧠 [dancinlab/hexa-mind](https://github.com/dancinlab/hexa-mind) — 7-verb mental substrate.
- 💎 [dancinlab/hexa-lang](https://github.com/dancinlab/hexa-lang) — the perfect-number programming language.

Upstream concept SSOT: `canon/{domains/life/agriculture,domains/life/apiculture,domains/life/aquaculture,domains/life/baking,domains/life/biochar-dryland-restoration,domains/life/cheese-dairy,domains/life/coffee,domains/life/coffee-science,domains/life/ecology,domains/life/ecology-agriculture-food,domains/life/entomology,domains/life/fermentation,domains/life/food-science,domains/life/horticulture,domains/life/mycology,domains/life/urban-farming,domains/life/viticulture,domains/life/wine-enology}/`.

---

## Status

**SPEC_CATALOG_ONLY at v0.1.0** — markdown spec library + .hexa CLI router. No verb
ships a working .hexa runtime module yet; this repo is the closed-form spec
catalog only.

---

## Verify

`hexa-farm` ships a 4-script SPEC_FIRST closure verifier in `verify/`. All
checks are real-engineering (file presence on disk, cross-source scoreboard
agreement) or real-limits-anchored (FAO/USDA/SCA/IUCN/WWF/IWSR external
authority sources from `LIMIT_BREAKTHROUGH.md`). Lattice arithmetic is
included as a §1.3-aux self-consistency check only — never as sole
verification, never applied to external entities (per
[`LATTICE_POLICY.md`](LATTICE_POLICY.md) §1.3 rule 1 and raw#10 C3).

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

---

## License

MIT. See [LICENSE](LICENSE).
