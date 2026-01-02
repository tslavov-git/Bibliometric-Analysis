# AI-Driven Cybersecurity in Critical Infrastructure (2015–2025) — Bibliometric Package

This repository contains the data and derived outputs used in the paper:

**“AI-Driven Cybersecurity in Critical Infrastructure: A Bibliometric Analysis (2015–2025)”**  
(Energy / Transport / Water sector stratification; OT/ICS/SCADA focus)

## Data sources
- **Scopus** (query executed in `TITLE-ABS-KEY`)
- **Web of Science Core Collection** (query executed in `TS` / Topic)
- Time window: **2015–2025**
- Document types: **Article** and **Proceedings Paper**
- Language: **English**

## Corpus construction (PRISMA-guided accounting)
1. Records were retrieved from Scopus and Web of Science using boolean queries designed around:
   - AI methods (e.g., machine learning, deep learning, federated learning, XAI)
   - OT/ICS/SCADA / critical infrastructure context
   - cybersecurity objectives (e.g., intrusion/anomaly/threat detection; false data injection)
2. Collections were created and merged in Biblioshiny/bibliometrix.
3. **Deduplication** was performed primarily via **DOI**, supported by title matching.
4. Final merged corpus size: **n = 1,862 unique documents**.

## Sector stratification
Sector tagging was performed using a rule-based multi-label approach on a concatenated metadata field:
- `TEXT_ALL = Title + Abstract + Author Keywords`

Three boolean flags were created:
- `Sector_Energy`
- `Sector_Transport`
- `Sector_Water`

Resulting sub-corpora (multi-label allowed):
- Energy: **N = 716**
- Transport: **N = 1,131**
- Water: **N = 233**

## Contents
### Core corpus
- `SCOPUS + WoS COLLECTIONS.xlsx` — merged, deduplicated dataset (n=1862)

### Sector subsets
- `Energy_Data.xlsx`
- `Transport_Data.xlsx`
- `Water_Data.xlsx`

### Bibliometric outputs (tables)
- `Most_Global_Cited_Documents_bibliometrix_2026-01-02.xlsx`
- `Thematic Evolution - TABLE.xlsx`
- `Thematic Map - TABLE - ENERGY.xlsx`
- `Thematic Map - Clusters - ENERGY.xlsx`
- `Thematic Map - TABLE - TRANSPORT (Author's keywords).xlsx`
- `Thematic Map - Clusters - TRANSPORT (Author's keywords).xlsx`
- `Thematic Map - TABLE - WATER (Author's keywords).xlsx`
- `Thematic Map - Clusters - WATER (Author's keywords).xlsx`

### Figures (black & white for conference submission)
- `Thematic Map - Author's keywords - TRANSPORT B&W.png`
- `Thematic Map - Author's keywords - WATER B&W.png`
- `Thematic Evolution - ENERGY B&W.png`
- `Thematic Map - ENERGY B&W.png`

## How to reproduce (high-level)
1. Import the Scopus/WoS collections into Biblioshiny/bibliometrix.
2. Merge collections and deduplicate (DOI + title match).
3. Create `TEXT_ALL` as Title+Abstract+Author Keywords and apply sector tagging rules.
4. For each sector subset, run conceptual structure / thematic map analysis using **Author Keywords**.
5. For Energy sector thematic evolution, run thematic evolution using **All Keywords** with a cut-point at 2020.

## Notes
- This repository is intended to provide access to the merged corpus and derived tables used to generate figures and results in the paper.
