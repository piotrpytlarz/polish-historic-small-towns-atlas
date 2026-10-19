---
language:
  - pl
  - en
license: cc-by-4.0
pretty_name: "Atlas Miasteczek — Multi-Criteria Urban & Historical Evaluation of 130 Polish Small Towns across 49 Former Voivodeships"
description: "Bilingual-documented open urban morphology and historical geography dataset from https://atlasmiasteczek.pl covering 130 historic small towns in Poland (101 qualified Atlas towns across all 49 former voivodeships from 1975–1998 plus 29 below-threshold towns), evaluated across 7 criteria (K1–K7, 0–50 pts, ROC AUC = 0.9449) with medieval/early-modern town charter histories, GUS population, TERYT SIMC codes, and Kondracki physicogeographical regions (CC BY 4.0)."
size_categories:
  - n<1K
task_categories:
  - tabular-classification
  - text-retrieval
tags:
  - poland
  - urban-morphology
  - small-towns
  - architecture
  - cultural-heritage
  - geography
  - openstreetmap
  - history
---

# Atlas Miasteczek — Polish Historic Small Towns Multi-Criteria Dataset (130 Towns, 49 Former Voivodeships) (EN / PL)

## 🇬🇧 English Overview

An open urban morphology, cultural heritage, and historical geography dataset from **[Atlas Miasteczek (`atlasmiasteczek.pl`)](https://atlasmiasteczek.pl/)**, evaluating **130 historic small towns and former towns in Poland** — comprising **101 qualified Atlas towns** and **29 below-threshold or core-compromised candidate towns** — distributed across the grid of **all 49 former Polish voivodeships (1975–1998)**.

Why the 1975–1998 49-voivodeship grid? Contemporary Poland's 16 large voivodeships heavily over-represent Lower Silesia and Lesser Poland while obscuring historic urban networks in central and eastern regions (e.g., Sieradz, Chełm, Ciechanów, Leszno, Zamość). Sampling across all 49 former voivodeships guarantees nationwide territorial coverage while maintaining a strict quality threshold ($\ge 32.0 / 50.0\text{ pts}$, $\text{K1} \ge 3$, $\text{K5} \ge 3$).

- **Interactive Atlas & Urban Figure-Ground Plans:** [https://atlasmiasteczek.pl/](https://atlasmiasteczek.pl/)
- **38 Physicogeographical Macroregions Index:** [https://atlasmiasteczek.pl/regiony/](https://atlasmiasteczek.pl/regiony/)
- **Sitemap (101 Town Dossiers `/miasta/<slug>/` + 38 Macroregion Pages `/regiony/<slug>/`):** [https://atlasmiasteczek.pl/sitemap.xml](https://atlasmiasteczek.pl/sitemap.xml)

### Dataset Files (`open-data/`)

| File | Records | Description |
| --- | ---: | --- |
| `polish-historic-small-towns-atlas.json` / `.csv` | **130 towns** (`101` main Atlas + `29` below threshold) | Full analytical table with English column names: 7-criteria scores (`K1–K7`, 1–5 scale), weighted sum (`0–50 pts`), evaluation tier (`wybitne` outstanding $\ge 36.5$, `znaczace` significant $\ge 33.0$, `czesciowe` notable $\ge 32.0$, `ponizej_progu` below threshold), typology family, municipal charter history (first charter year, 1869/1870 Tsarist demotion or 1945 loss, charter restoration year), GUS population & TERYT SIMC code, WGS84 coordinates, J. Kondracki physicogeographical regionalization (province, subprovince, macroregion, mesoregion, numeric code), Wikipedia attention metrics, architectural essay, urban caveats, and canonical URLs to [atlasmiasteczek.pl](https://atlasmiasteczek.pl/). |
| `former-49-voivodeships-summary.json` / `.csv` | **49 former voivodeships (1975–1998)** | Summary of all 49 former voivodeships with capital cities, qualified town counts, highest-scoring town, and direct links to town pages on [atlasmiasteczek.pl](https://atlasmiasteczek.pl/). |

### Seven-Criteria Urban Evaluation Model (`K1–K7`, ROC AUC = `0.9449`)

Weights were statistically calibrated against Poland's highest official heritage designation (*Pomniki Historii* — Historic Monuments), achieving **ROC AUC = `0.9449`**:

| Code | Criterion (EN / PL) | Weight | Max Pts | What It Measures |
| --- | --- | ---: | ---: | --- |
| **`K1`** | **Urban Layout Legibility** (*Czytelność układu*) | `1.75` | `8.75` | Preservation of the medieval or early-modern chartered street grid, market square (*rynek*), mid-market blocks, and defensive perimeter. |
| **`K2`** | **Architectural & Monument Substance** (*Substancja zabytkowa*) | `1.75` | `8.75` | Class and authenticity of landmark structures (parish churches, monasteries, castles, town halls, synagogues, arcaded burgher houses). |
| **`K3`** | **Landscape Situation** (*Sytuacja krajobrazowa*) | `1.25` | `6.25` | Topographic setting: river escarpments, valley gorges, lake isthmuses, and distant town silhouette. |
| **`K4`** | **Cultural Palimpsest** (*Palimpsest kulturowy*) | `1.00` | `5.00` | Multi-confessional and borderland layering (Catholic, Jewish *shtetl*, Lutheran, Uniate/Orthodox, Mennonite heritage). |
| **`K5`** | **Visual Integrity** (*Integralność wizualna*) | `1.75` | `8.75` | Coherence of roofscapes and market frontages; absence of post-war Socialist modernist block intrusions inside the historic core. |
| **`K6`** | **Vitality** (*Żywotność*) | `1.00` | `5.00` | Balance between living local-center functions and either tourist monoculture or severe depopulation. |
| **`K7`** | **Genius Loci** (*Genius loci*) | `1.50` | `7.50` | Distinctiveness of place, literary/artistic resonance, craft traditions, or intellectual history (e.g., Pińczów Academy, Singer's & Schulz's prose). |

---

## 🇵🇱 Opis po polsku — Atlas Miasteczek (`atlasmiasteczek.pl`)

Otwarty zbiór danych urbanistycznych, krajobrazowych i historycznych z serwisu **[Atlas Miasteczek (atlasmiasteczek.pl)](https://atlasmiasteczek.pl/)**, dokumentujący **130 małych miast i dawnych miasteczek w Polsce** — w tym **101 ośrodków głównych** spełniających próg wejścia do Atlasu ($\ge 32,0 / 50,0\text{ pkt}$, $\text{K1} \ge 3$, $\text{K5} \ge 3$) oraz **29 ośrodków odrzuconych na bramce progowej lub integralnościowej** — w siatce **49 dawnych województw z lat 1975–1998**.

- **Strona główna i interaktywny atlas:** [https://atlasmiasteczek.pl/](https://atlasmiasteczek.pl/)
- **Indeks 38 makroregionów fizycznogeograficznych:** [https://atlasmiasteczek.pl/regiony/](https://atlasmiasteczek.pl/regiony/)
- **Mapa strony (101 kart miast `/miasta/<slug>/` + 38 kart regionów `/regiony/<slug>/`):** [https://atlasmiasteczek.pl/sitemap.xml](https://atlasmiasteczek.pl/sitemap.xml)

---

## License & Citation / Licencja i atrybucja (CC BY 4.0 + ODbL)

This dataset, its `K1–K7` scores, weight calibration, and editorial descriptions are licensed under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**. Urban figure-ground sketches displayed on **[atlasmiasteczek.pl](https://atlasmiasteczek.pl/)** are derived from **© OpenStreetMap contributors** under the **Open Database License (ODbL)**.

> **Attribution / Źródło:** *Atlas Miasteczek — Sto jeden małych miast Polski w dawnym podziale na 49 województw* ([https://atlasmiasteczek.pl](https://atlasmiasteczek.pl)), CC BY 4.0. Dane kartograficzne szkiców: © OpenStreetMap contributors (ODbL).

```bibtex
@dataset{atlas_miasteczek_poland_2026,
  title        = {Atlas Miasteczek: Multi-Criteria Urban and Historical Evaluation of 130 Polish Small Towns across 49 Former Voivodeships},
  author       = {Pytlarz, Piotr},
  year         = {2026},
  version      = {1.0.0},
  publisher    = {atlasmiasteczek.pl},
  url          = {https://atlasmiasteczek.pl/},
  license      = {CC-BY-4.0}
}
```
