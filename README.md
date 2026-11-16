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

The architecture rests on four open pillars. The private `ru_*` service suite that
runs statbook.io — API, ledger, reconciliation, reporting — is built on top of them.

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

The platform is operated by an autonomous four-seat agent crew running 24/7 on a
two-GPU box: **Aldric** (manager), **Émile** (sub-manager), **Luca** (coder),
**Soren** (reviewer). Work routes through a shared inbox state machine; a root
thermal guard keeps the GPUs, drives, and CPU in safe bands. I own the merge button.

---

## Personal

| Repo | What it does |
|---|---|
| [`omarchytv`](https://github.com/MrCartaaa/omarchytv) | Omarchy-styled tiling launcher ecosystem for Android TV, Google TV, LG webOS, Android, and Linux/macOS |
| [`omarchy-tv-samsung`](https://github.com/MrCartaaa/omarchy-tv-samsung) | Deactivates ads and analytics on a Samsung TV |
| [`zero2prod`](https://github.com/MrCartaaa/zero2prod) | Rust — zero to production service experiments |
| [`atomics_locks`](https://github.com/MrCartaaa/atomics_locks) | Rust — lock-free atomics playground |
| [`cdn-tax`](https://github.com/MrCartaaa/cdn-tax) | Rust — tax computation on CDN billing |
| [`pdf-viewer`](https://github.com/MrCartaaa/pdf-viewer) | Pure-Python PDF viewer |
| [`llama`](https://github.com/MrCartaaa/llama) | llama.cpp deployments — local LLM serving on 2× TITAN RTX |

---

**Stack:** Rust · Angular · Flutter · PostgreSQL · Kubernetes · GitOps
**Principle:** the books must be right, and the machines must be boring.
