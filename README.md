# Carter

![Rust](https://img.shields.io/badge/Rust-orange?logo=rust&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?logo=angular&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)

**Bookkeeper with 10+ years in fintech. I build the systems that run the books.**

I run [Statbook.io](https://statbook.io) — live ops data from field → office →
decisions: health & safety, people, finance, and project control, delivered as a
service. COR™-aligned safety systems that hold up under audit, hiring and onboarding
playbooks, timesheets and attendance, job costing, and decision-ready books. I build
and lead the team that ships it — a Rust microservice platform on an Angular
frontend, deployed with GitOps, and coordinated by an autonomous agent crew.

---

## [Mae-Technologies](https://github.com/Mae-Technologies) — the platform, open core

The architecture rests on four open pillars. The private service suite that runs
statbook.io — API, ledger, reconciliation, reporting — is built on top of them.

| Pillar | What it does |
|---|---|
| [`mae`](https://github.com/Mae-Technologies/mae) | Shared Rust runtime — app, repo, posting, middleware, session, testing |
| [`mae_macros`](https://github.com/Mae-Technologies/mae_macros) | Procedural macros — `#[run_app]`, `#[schema]`, `#[mae_test]`, `MaeRepo` |
| [`postgres-mae`](https://github.com/Mae-Technologies/postgres-mae) | PG image + spec-driven DDL, ACL, and audit — services never raw-`CREATE` |
| [`rust_template`](https://github.com/Mae-Technologies/rust_template) | Service blueprint; every new service starts from it |

| Repo | What it does |
|---|---|
| [`cdn-payroll`](https://github.com/Mae-Technologies/cdn-payroll) | Canadian payroll crate — CRA deduction formulas (CPP, EI, Ontario), year-aware context |
| [`worldline_api`](https://github.com/Mae-Technologies/worldline_api) | Worldline payments integration |

---

## Agent team

**The platform is operated 24/7 by a four-seat autonomous crew** running on a
two-GPU box. Work flows through a shared inbox state machine — no seat acts on
assumption, and nothing moves without a record.

| Seat | Role | Mandate |
|---|---|---|
| **Aldric** | Manager | Talks to me. Splits work, tracks state, opens PRs, reports status. Never writes code. |
| **Émile** | Sub-manager | Claims work from the inbox and routes it — code to Luca, review to Soren. |
| **Luca** | Coder | Implements the issue, runs the gates (analyze, test, build), pushes the branch, opens the PR, then flips the ticket to done. |
| **Soren** | Reviewer | Reviews the actual PR and leaves a formal GitHub review — approve or request changes. |

**Chain:** `assigned → in_progress → done → in_review → review_passed → approved → pr_open → merged`

Every transition has a named actor and lands in a shared audit log. Three invariants
keep it honest:

- the coder opens the PR **before** `done` — what gets reviewed is what gets merged
- the reviewer's verdict is a GitHub review, not a chat message
- `merged` is only recorded after I merge; the agents never touch `main`

**Keeping the machine quiet:** a root-level thermal guard watches the drives, GPUs,
and CPU every two minutes — when the box runs hot it holds the seats, and releases
them when it cools. Each seat wakes on a 30-minute systemd timer. No polling, no
babysitting.

---

## Personal

| Repo | What it does |
|---|---|
| [`omarchytv`](https://github.com/MrCartaaa/omarchytv) | Omarchy-styled tiling launcher ecosystem for Android TV, Google TV, LG webOS, Android, and Linux/macOS |
| [`omarchy-tv-samsung`](https://github.com/MrCartaaa/omarchy-tv-samsung) | Deactivates ads and analytics on a Samsung TV |
| [`zero2prod`](https://github.com/MrCartaaa/zero2prod) | Rust — zero to production service experiments |
| [`atomics_locks`](https://github.com/MrCartaaa/atomics_locks) | Rust — lock-free atomics playground |
| [`cdn-tax`](https://github.com/MrCartaaa/cdn-tax) | Rust — tax computation on CDN billing |


---

**Stack:** Rust · Angular · Flutter · PostgreSQL · Kubernetes · GitOps
**Principle:** the books must be right, and the machines must be boring.
