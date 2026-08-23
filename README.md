# Kennel

**Breeder Hub** — Web calculator tracking genetic mechanics for pet breeding across the 210 kinds.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) ecosystem. Index: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. This repository ships the contract, README, and layout so implementation can start without renaming the organ later.

## Why it exists

Lineages matter. Kennel shows what two pets can produce, what is canon-illegal (panda × fish), and the rarity of a whelp before anyone mints it.

The flagship overlay already puts a living sticker on the real desktop (Rui first, 210 kinds). Kennel does not replace that. It is one organ.

## Stack

TypeScript · React 19 · Vite · genetic calculator · Spring lineage API

GroupId / namespace: `com.enterprisepet.kennel`  
Default listen: `8080`

## Talks to

- computerpets-lore
- computerpets-minter
- computerpets-ledger
- computerpets Spring pet records

## Contract

### Data

`Pairing(a, b, legal) · WhelpRow(trait, p) · Lineage(nodes[], coeff)`

### Surface

- POST /v1/predict — two petIds → whelp table + illegal flag
- GET /v1/lineage/{petId} — ancestors, generation, inbreeding coeff
- GET /v1/species-matrix — who can breed with whom

### Failure doctrine

Illegal pair → explain, never invent a hybrid species. Missing parent NFT → mark lineage broken, not 'unknown panda'.

## Layout

```
computerpets-kennel/
  README.md           this file
  LICENSE             MIT
  docs/CONTRACT.md    the same contract, frozen for implementers
  src/                implementation lands here
```

## Run (Windows)

PowerShell, from this folder, after the flagship helpers (Git, Node LTS 22+, JDK 21 as needed):

```powershell
cd app; npm install; npm run dev
```

You do not need this service to meet Rui. The [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md) is still the first pet.

## Ecosystem

| Organ | Repo |
| --- | --- |
| Flagship desktop + Spring | [RicheyWorks/computerpets](https://github.com/RicheyWorks/computerpets) |
| This organ | [RicheyWorks/computerpets-kennel](https://github.com/RicheyWorks/computerpets-kennel) |
| Full map | [RicheyWorks/computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem) |

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
