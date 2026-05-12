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

## License

MIT. See [LICENSE](LICENSE).
