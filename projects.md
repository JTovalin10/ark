# Systems Engineer Project Roadmap

UW CSE '27 · Target: GCP, AWS, Cloudflare, Red Hat · Apply fall 2026

---

## Core Projects (Must Do)

### 1. Raft KV Store in Go
Primary distributed systems portfolio piece. Built on the Paxos foundation from 452 — conceptually familiar, but implementation details differ enough to require reading Figure 2 carefully.

- **Phase 1 + 2** (leader election, log replication, KV store layer) — complete by mid-summer
- **Phase 3** (sharding) — complete by end of fall senior year
- Well-tested, well-documented, public GitHub repo with a strong README explaining architecture and design decisions

### 2. Linux Kernel Scheduler Contributions
Ongoing throughout everything. Start reading `kernel/sched/` now. Runs in parallel with all other work — one hour per week minimum, more when available.

- First patch submitted — end of summer
- First patch accepted — end of fall

---

## If You Have Time

### 3. etcd Contribution
Do this spring semester after Raft Phase 3 is solid.

One meaningful PR to etcd creates the strongest possible GCP narrative: you built Raft from scratch, then contributed to the production Raft implementation that runs Kubernetes. GCP engineers know the etcd codebase personally. A merged PR there is a stronger signal than any personal project because it was reviewed and approved by world-class engineers.

Find a good first issue. Read the etcd Raft implementation alongside your own. Understand where they diverge and why.

---

## Complete Timeline

| Period | Project Work | Applications |
|---|---|---|
| Now → May | Read Raft paper, create `raft-kv` repo skeleton, start reading `kernel/sched/` | Email uncle, warm up GCP contact |
| June → August | Raft Phase 1 + 2 at Truveta (1hr/day), first kernel patch submitted | GCP opens August — apply immediately |
| September → December | Raft Phase 3, first kernel patch accepted, TA-ing, 453 + Rust course | Apply AWS, Azure, Cloudflare, Red Hat, Meta PE, Databricks |
| January → March | Polish all READMEs, start etcd contribution, interview prep intensifies | Interview season |
| April → June | etcd PR if not done, interview prep only — no new projects | Accept offer |
| Post-graduation | Custom memory allocator, QUIC, Stanford HCP application | — |

---

## What You Graduate With

- **Sharded Raft KV store in Go** — original distributed systems work
- **Linux kernel scheduler patches** — OS depth at the lowest level
- **etcd contribution** — production systems credibility
- **DNS server in C** — networking fundamentals shipped
- **Thread pool + lock-free data structures in C++** — concurrency depth
- **UW 451/452/453/461 systems sequence** — academic foundation
- **TA-ing OS or systems programming** — faculty letter + teaching depth

Every project tells the same story: systems engineer who operates from the kernel level up to distributed systems. That's exactly the profile GCP, AWS, Azure, Cloudflare, and Red Hat are hiring for.
