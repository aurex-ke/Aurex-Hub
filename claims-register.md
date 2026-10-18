# Claims register

Single source of truth. Every claim on any page must have a row here.

**Labels:** Completed (evidence linked), Simulated (reproducible seeded run linked), Planned (not done), Unverified (draft only; must be zero before publishing).

Last reviewed: 2026-10-18  
Unverified rows: 0

| ID | Claim | Status | Evidence | Source and retrieval date | Notes |
|---|---|---|---|---|---|
| C-001 | Diploma in Electrical and Electronic Engineering (Power option), Machakos Institute of Technology, expected 2027 | Planned | None (self-reported) | n/a | Word as "expected 2027, self-reported" |
| C-002 | Microsoft IoT for Beginners retake: 0 of 24 lessons | Planned | None | Microsoft Tech Community blog; Raspberry Pi Foundation post; retrieved 2026-10-13 | "12 weeks" is the course design length. Virtual hardware (CounterFit) confirmed in the Microsoft blog. No certificate found. Lesson-to-milestone mapping not yet verified. Official repo README seen only via mirrors |
| C-003 | Scrimba Fullstack Developer Path (scrimba.com) retake, none completed | Planned | None | scrimba.com/c0fullstack; Scrimba article "Best Full-Stack Developer Courses [2026]"; retrieved 2026-10-13 | Not the Coursera specialization (user confirmed 2026-10-13). Duration conflict: 105.8 h (path page) vs 108.4 h, 20 modules (article). Path page lists a Certificate of Completion: not earned, not claimed. Database module names unconfirmed |
| C-004 | OpenEMS Edge and its built-in UI run in Docker Compose with a small simulated example (a household load profile, a battery and a balancing controller; not the hotel) | Completed | [Commit 4e01b61](https://github.com/aurex-ke/ke-designated-facility-ems/commit/4e01b61) | OpenEMS Getting Started guide and Simulated Components page, retrieved 2026-10-16; start-up script of the pinned Edge image, read 2026-10-16; terminal output of `git push` and `git log --oneline -1` showing HEAD and origin/main at 4e01b61, reported by the owner 2026-10-18 | One tested setup: Ubuntu Server 26.04 (amd64) in a UTM virtual machine on an Intel Mac. The smoke test passed on the long-running stack, after a container recreate, after clean reboots and on fresh volumes (2026-10-16 to 2026-10-17); see the venture runbook. After an abrupt VM stop on 2026-10-16 the log reads failed until the containers were recreated (cause unproven, runbook section 9). Default logins are used in development only (ADR 0005). Unresolved: the cause of the 2026-10-15 VM freezes, the cause of a 5-minute "defective app" message on fresh volumes, and whether the simulated load is reproducible between starts. Edge and UI licence statements were still seen only through mirrors. The commit URL was opened by the owner and works (screenshot of the commit page reported 2026-10-18) |
| C-005 | Tariff model and peak-shifting scenario | Planned | None | Not yet checked | Tariff values are assumptions |
| C-006 | Compliance report for a designated facility | Planned | None | Kenya Law excerpts, retrieved 2026-10-13 (see venture problem statement) | Excerpts confirm: 180,000 kWh threshold, audit at least every 4 years, report within 1 month, 50% of savings within 3 years of the investment plan. Full text not read (site blocked automated fetch). Net-metering caps corrected: domestic 4 kW single-phase or 10 kW three-phase, C&I capped at maximum demand, below 1 MW applicability. Export credit rate: leave unstated. "Dumping" and the September 2026 amendment unverified. Auditor independence unverified |
| C-007 | Simulated 60-room hotel `hotel-60rooms-sim-v1` | Planned | None | n/a | Size, load profile and threshold status are assumptions |
| C-008 | Venture repository documentation (README, problem statement, ADRs 0001 and 0002) published for milestone M1 | Completed | [Commit 41feb60](https://github.com/aurex-ke/ke-designated-facility-ems/commit/41feb60) | Terminal output of `git log --oneline -1` showing HEAD and origin/main at 41feb60, reported by the owner 2026-10-13 | Documentation only, no code. The commit URL was opened by the owner and works (reported 2026-10-13) |

## Not claimed

Deployments, pilots, partners, users, contributors, stars, certificates, completed courses, real facility data, legal advice, and any affiliation with OpenEMS, Microsoft or Scrimba.

## Re-verify at H4

Regulatory thresholds and dates (read the full legal text), licences of third-party material (including the IoT for Beginners LICENSE file and the OpenEMS licence files), Microsoft and Scrimba course pages, all external links.
