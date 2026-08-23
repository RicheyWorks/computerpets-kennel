# Kennel contract

Do not implement against folklore. Implement against this file.

## Identity

- Product: **Kennel**
- Repo: `computerpets-kennel`
- Category: Web & Client
- Idea: Breeder Hub
- Port / surface: `8080`

## Must

- Stay canon with 210 species. No illegal hybrids. No swapped voices.
- Treat the desktop overlay as the main quest. This organ is optional until wired.
- Fail soft: the overlay keeps walking if this service is down, unless this *is* the overlay.
- No PII in public artifacts (Steam id, wallet, home path, webcam frames).

## Data

Pairing(a, b, legal) · WhelpRow(trait, p) · Lineage(nodes[], coeff)

## Surface

- POST /v1/predict — two petIds → whelp table + illegal flag
- GET /v1/lineage/{petId} — ancestors, generation, inbreeding coeff
- GET /v1/species-matrix — who can breed with whom

## Neighbors

- computerpets-lore
- computerpets-minter
- computerpets-ledger
- computerpets Spring pet records

## Failure doctrine

Illegal pair → explain, never invent a hybrid species. Missing parent NFT → mark lineage broken, not 'unknown panda'.

## Stack

TypeScript · React 19 · Vite · genetic calculator · Spring lineage API
