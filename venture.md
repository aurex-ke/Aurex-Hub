# Venture: ke-designated-facility-ems

**Status:** M1 Completed; M2 to M8 Planned  
**Claim IDs:** C-004, C-005, C-006, C-007, C-008

Repository: https://github.com/aurex-ke/ke-designated-facility-ems

## What I did

- Published the M1 documentation set to the venture repository: README, problem statement and two architecture decision records (commit `41feb60`).
- Checked regulation excerpts and OpenEMS licence statements while writing them (2026-10-13). Details and gaps are in the problem statement.

No code exists. Nothing is deployed. There are no pilots, partners or users.

## What the project is

An open-source, simulation-first reference implementation of an energy management system (EMS) for Kenyan designated facilities. The v0.1 scenario is a simulated 60-room hotel (`hotel-60rooms-sim-v1`). OpenEMS Edge handles PV and storage control in its simulated environment, and a separate Python layer handles ingestion, sub-metering, tariffs and compliance reporting. Hotel size, load profile, tariffs and threshold status are assumptions to be calibrated against real bills.

## Milestones

| ID | Milestone | Status | Evidence |
|---|---|---|---|
| M1 | Repo, README, problem statement, architecture decision records | Completed | [Commit 41feb60](https://github.com/aurex-ke/ke-designated-facility-ems/commit/41feb60) |
| M2 | OpenEMS Edge with simulators in Docker Compose | Planned | None |
| M3 | Hotel load generator and sub-meter data | Planned | None |
| M4 | Ingestion and storage | Planned | None |
| M5 | Tariff model and one peak-shifting scenario | Planned | None |
| M6 | Compliance report | Planned | None |
| M7 | Write-up of results | Planned | None |
| M8 | Optional Jetson Nano hardware validation (never required) | Planned | None |

Out of scope for v0.1: utility API, authentication, multi-site, real hardware, billing, M-Pesa, custom dashboard.

## Evidence

M1: commit [`41feb60`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/41feb60) on `main`. M2 to M8: none yet.

## How it connects

Each skill from my [learning pages](learning/) maps to a milestone in the [skills map](skills-map.md). The order of work is in [milestones](milestones.md).

## How to help

- Review the regulation summary in the venture repository's problem statement against the full legal text, and open an Issue with a source for any correction.
- Suggest realistic hotel load profile references, with sources.
- Point out OpenEMS simulator components that fit PV and storage, citing the official documentation.

## Known gaps

- Regulation facts were checked against excerpts. The full legal text was not read because the source blocked automated access.
- The export credit rate is deliberately unstated. Sources disagree and it has not been checked against the regulation text.
- OpenEMS component names, drivers and controllers are not yet checked. M2 starts with the official documentation.
- OpenEMS licence statements were seen through third-party mirrors, not the official repository.
- All hotel and tariff numbers are assumptions.

## Not claimed

Deployments, pilots, partners, users, contributors, stars, real facility data, legal advice, and any affiliation with or endorsement by OpenEMS.

## Sources

- Venture repository: https://github.com/aurex-ke/ke-designated-facility-ems
- Problem statement (sources and retrieval dates are listed there): `docs/problem-statement.md` in the venture repository
