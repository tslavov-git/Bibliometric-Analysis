# Deduplication log (PRISMA-guided accounting)

## Data sources
- Scopus
- Web of Science Core Collection

## Time window used in the paper
- 2015–2025

## Imported records
- Scopus import: **n = 1,774** (`SCOPUS COLLECTION.xlsx`)
- WoS import: **n = 971** (`WoS COLLECTION.xlsx`)
- Total before deduplication: **n = 2,745**

## Deduplication tooling
- R (RStudio), `bibliometrix` package via the Biblioshiny interface

## Deduplication rule (high-level)
- Primarily DOI-based matching, supported by title-based matching

## Deduplication outcome
- Duplicates removed: **n = 883**
- Final merged corpus: **n = 1,862** (`SCOPUS + WoS COLLECTIONS.xlsx`)
- Final corpus composition (`DB_Original`):
  - Scopus: **n = 892**
  - WoS / ISI: **n = 970**

## Notes
- Thematic evolution analysis uses a cut-point at **2020** (2015–2020 vs 2021–2025).
- The merged dataset contains a small number of 2026-indexed records; analyses in the paper are restricted to **2015–2025**.
