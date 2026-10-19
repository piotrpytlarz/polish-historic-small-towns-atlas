---
language:
  - pl
license: cc-by-4.0
pretty_name: "Atlas Miasteczek — Multi-Criteria Urban & Historical Evaluation of 130 Polish Small Towns across 49 Former Voivodeships"
description: "Otwarty zbiór danych urbanistyczno-historycznych z serwisu https://atlasmiasteczek.pl obejmujący 130 małych miast i dawnych miasteczek w Polsce (101 ośrodków zakwalifikowanych do Atlasu w podziale na 49 dawnych województw z lat 1975–1998 oraz 29 ośrodków poniżej progu wejścia), ocenionych w 7 kryteriach (K1–K7, 0–50 pkt) wraz z historią praw miejskich, regionalizacją fizycznogeograficzną Kondrackiego i kodami TERYT."
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

# Atlas Miasteczek — Polish Historic Small Towns Multi-Criteria Dataset (130 Towns, 49 Former Voivodeships)

Otwarty zbiór danych urbanistycznych, krajobrazowych i historycznych z serwisu **[Atlas Miasteczek (atlasmiasteczek.pl)](https://atlasmiasteczek.pl/)**, dokumentujący **130 małych miast i dawnych miasteczek w Polsce** — w tym **101 ośrodków głównych** spełniających próg wejścia do Atlasu oraz **29 ośrodków odrzuconych na bramce progowej lub integralnościowej** — w siatce **49 dawnych województw z lat 1975–1998**.

- **Strona główna i interaktywny atlas:** [https://atlasmiasteczek.pl/](https://atlasmiasteczek.pl/)
- **Indeks 38 makroregionów fizycznogeograficznych:** [https://atlasmiasteczek.pl/regiony/](https://atlasmiasteczek.pl/regiony/)
- **Mapa strony (101 kart miast `/miasta/<slug>/` + 38 kart regionów `/regiony/<slug>/`):** [https://atlasmiasteczek.pl/sitemap.xml](https://atlasmiasteczek.pl/sitemap.xml)

---

## Zawartość pakietu (`open-data/`)

| Plik | Liczba rekordów | Opis zawartości |
| --- | ---: | --- |
| `polish-historic-small-towns-atlas.json` / `.csv` | **130 miasteczek** (101 w Atlasie + 29 poniżej progu) | Pełna tabela analityczna: oceny w 7 kryteriach (`K1–K7`, skala 1–5), suma ważona (`0–50 pkt`), klasa oceny (`wybitne`, `znaczace`, `czesciowe`, `ponizej_progu`), rodzina typologiczna, historia praw miejskich (rok pierwszej lokacji, utraty w 1869/1870 lub 1945, odzyskania), ludność GUS i kod TERYT SIMC, współrzędne geograficzne, regionalizacja fizycznogeograficzna J. Kondrackiego (prowincja, podprowincja, makroregion, mezoregion, kod cyfrowy), metryki rozpoznawalności oraz szkic eseistyczny i zastrzeżenia urbanistyczne wraz z kanonicznymi linkami URL do [atlasmiasteczek.pl](https://atlasmiasteczek.pl/). |
| `former-49-voivodeships-summary.json` / `.csv` | **49 województw (1975–1998)** | Zestawienie wszystkich 49 dawnych województw (od bialskopodlaskiego po zielonogórskie) z liczbą zakwalifikowanych ośrodków, liderem punktowym i bezpośrednimi linkami do kart miast w serwisie [atlasmiasteczek.pl](https://atlasmiasteczek.pl/). |

---

## Siedmiokryterialny model oceny urbanistycznej (`K1–K7`)

Podział na 49 dawnych województw (1975–1998) zastosowano celowo jako filtr antycentralistyczny: współczesne 16 dużych województw faworyzuje Dolny Śląsk i Małopolskę kosztem dawnych ziem sieradzkiej, chełmskiej, ciechanowskiej czy leszczyńskiej. W każdym z 49 województw oceniono kandydatów w **7 kryteriach w skali 1–5**, których wagi skalibrowano statystycznie (ROC AUC = `0.9449` względem zewnętrznego kanonu ochrony konserwatorskiej — Pomników Historii):

| Kod | Kryterium | Waga | Maks. pkt | Co mierzy |
| --- | --- | ---: | ---: | --- |
| **`K1`** | **Czytelność układu** | `1,75` | `8,75` | Zachowanie średniowiecznego lub nowożytnego planu lokacyjnego (rynek, bloki śródrynkowe, sieć ulic, obrys murów). |
| **`K2`** | **Substancja zabytkowa** | `1,75` | `8,75` | Ranga i autentyzm kluczowych budowli (fary, klasztory, zamki, ratusze, synagogi, kamienice podcieniowe). |
| **`K3`** | **Sytuacja krajobrazowa** | `1,25` | `6,25` | Osadzenie w rzeźbie terenu: skarpa nadrzeczna, przełom rzeki, przesmyk między jeziorami, sylweta z dystansu. |
| **`K4`** | **Palimpsest kulturowy** | `1,00` | `5,00` | Wielość nawarstwień wyznaniowych, etnicznych i granicznych (ślady żydowskie, ewangelickie, unickie, prawosławne, mennonickie). |
| **`K5`** | **Integralność wizualna** | `1,75` | `8,75` | Spójność skali i pierzei rynkowych, brak powojennych wyrw i dysharmonijnej zabudowy blokowej w rdzeniu historycznym. |
| **`K6`** | **Żywotność** | `1,00` | `5,00` | Równowaga między funkcją lokalnego ośrodka życia a monokulturą turystyczną lub głębokim wyludnieniem. |
| **`K7`** | **Genius loci** | `1,50` | `7,50` | Swoistość miejsca, zakorzenienie w literaturze, sztuce, rzemiośle lub historii idei (np. Akademia Pińczowska, proza Singera i Schulza). |

**Bramka wejścia do Atlasu (101 miast):** Suma ważona $\ge 32,0 / 50,0\text{ pkt}$ przy jednoczesnym spełnieniu warunków brzegowych $\text{K1} \ge 3$ (czytelny układ) oraz $\text{K5} \ge 3$ (niezdewastowany rdzeń).

---

## Licencja i atrybucja (CC BY 4.0 + ODbL)

Zbiór danych, punktacja `K1–K7`, kalibracja wag oraz opisy autorskie są udostępniane na licencji **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**. Szkice urbanistyczne na stronach poszczególnych miast w serwisie **[atlasmiasteczek.pl](https://atlasmiasteczek.pl/)** powstają na podstawie danych **© OpenStreetMap contributors** udostępnianych na licencji **Open Database License (ODbL)**.

Przy wykorzystaniu zbioru w publikacjach, analizach geograficznych lub projektach wizualizacyjnych prosimy o podanie atrybucji z aktywnym linkiem:

> **Źródło:** *Atlas Miasteczek — Sto jeden małych miast Polski w dawnym podziale na 49 województw* ([https://atlasmiasteczek.pl](https://atlasmiasteczek.pl)), licencja CC BY 4.0. Dane kartograficzne szkiców: © OpenStreetMap contributors (ODbL).

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
