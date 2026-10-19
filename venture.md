# Venture: ke-designated-facility-ems

**Status:** M1 and M2 Completed; M3 to M8 Planned  
**Claim IDs:** C-004, C-005, C-006, C-007, C-008, C-009

Repository: https://github.com/aurex-ke/ke-designated-facility-ems

## What I did

- Published the M1 documentation set to the venture repository: README, problem statement and two architecture decision records (commit `41feb60`).
- Checked regulation excerpts and OpenEMS licence statements while writing them (2026-10-13). Details and gaps are in the problem statement.
- Built the simulated Edge stack in Docker Compose: images pinned by digest, a seed for a small simulated chain, a smoke test and a runbook (commits `f11c625`, `48c6333`, `6cbd47d`, `a26ae34`, `4e01b61`).
- Found a seed-order bug with a fresh-volume test, fixed it, and wrote the unresolved observations into the runbook instead of guessing their causes.
- Added contribution files to the venture repository: a contributing guide, a security policy that uses GitHub's private vulnerability reporting, a code of conduct that adopts the Contributor Covenant 3.0 by link, and two issue forms (commits `eb6e858`, `5a5d435`, `3d5720b`).

No Python code exists yet. The Compose files and a shell smoke test do. Nothing is deployed. There are no pilots, partners or users.

## What the project is

An open-source, simulation-first reference implementation of an energy management system (EMS) for Kenyan designated facilities. The v0.1 scenario is a simulated 60-room hotel (`hotel-60rooms-sim-v1`). OpenEMS Edge handles PV and storage control in its simulated environment, and a separate Python layer handles ingestion, sub-metering, tariffs and compliance reporting. Hotel size, load profile, tariffs and threshold status are assumptions to be calibrated against real bills.

## Milestones

| ID | Milestone | Status | Evidence |
|---|---|---|---|
| M1 | Repo, README, problem statement, architecture decision records | Completed | [Commit 41feb60](https://github.com/aurex-ke/ke-designated-facility-ems/commit/41feb60) |
| M2 | OpenEMS Edge with simulators in Docker Compose | Completed | [Commit 4e01b61](https://github.com/aurex-ke/ke-designated-facility-ems/commit/4e01b61) |
| M3 | Hotel load generator and sub-meter data | Planned | None |
| M4 | Ingestion and storage | Planned | None |
| M5 | Tariff model and one peak-shifting scenario | Planned | None |
| M6 | Compliance report | Planned | None |
| M7 | Write-up of results | Planned | None |
| M8 | Optional Jetson Nano hardware validation (never required) | Planned | None |

Out of scope for v0.1: utility API, authentication, multi-site, real hardware, billing, M-Pesa, custom dashboard.

## Evidence

M1: commit [`41feb60`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/41feb60) on `main`. M2: commit [`4e01b61`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/4e01b61) on `main`, with the runbook and ADRs 0003 to 0005 in the same repository. Contribution files: commits [`eb6e858`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/eb6e858), [`5a5d435`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/5a5d435) and [`3d5720b`](https://github.com/aurex-ke/ke-designated-facility-ems/commit/3d5720b). M3 to M8: none yet.

## How it connects

Each skill from my [learning pages](learning/) maps to a milestone in the [skills map](skills-map.md). The order of work is in [milestones](milestones.md).

## How to help

- Review the regulation summary in the venture repository's problem statement against the full legal text, and open an Issue with a source for any correction.
- Suggest realistic hotel load profile references, with sources.
- Point out OpenEMS simulator components that fit PV and storage, citing the official documentation.
- Run the stack from the runbook on another machine (Linux, or a Mac that Docker Desktop supports) and open an Issue with what happened.

## Known gaps

- Regulation facts were checked against excerpts. The full legal text was not read because the source blocked automated access.
- The export credit rate is deliberately unstated. Sources disagree and it has not been checked against the regulation text.
- The OpenEMS components used so far (a CSV datasource, a grid meter, a battery simulator, a balancing controller and a debug log) come from the official Getting Started guide. PV simulation, meters for sub-metering, drivers and other controllers are not yet checked.
- OpenEMS licence statements were seen through third-party mirrors, not the official repository.
- All hotel and tariff numbers are assumptions.
- The M2 stack was tested on one setup only: Ubuntu Server 26.04 (amd64) in a UTM virtual machine on an Intel Mac.
- The simulated example uses a household load profile, and its battery drains because the chain has no PV. Whether the simulated load is reproducible between starts is not established.
- The cause of two VM freezes on 2026-10-15 was never proven. A configuration change may have stopped them, or it may be luck.
- A "defective app" message appears for about 5 minutes after the first start on a fresh volume. Its cause is unknown.
- The development stack uses OpenEMS's documented default logins, on loopback only. This is recorded as a development-only exception (ADR 0005).
- The contribution files have not been used by anyone else. The reporter's view of private vulnerability reporting has not been tested.

## Not claimed

Deployments, pilots, partners, users, contributors, stars, real facility data, legal advice, and any affiliation with or endorsement by OpenEMS.

## Sources

- Venture repository: https://github.com/aurex-ke/ke-designated-facility-ems
- Problem statement (sources and retrieval dates are listed there): `docs/problem-statement.md` in the venture repository
- Runbook and ADRs 0003 to 0005 (sources and retrieval dates are listed there): `docs/runbook.md` and `docs/adr/` in the venture repository
- OpenEMS Getting Started guide: https://openems.github.io/openems.io/openems/latest/gettingstarted.html (retrieved 2026-10-16)
