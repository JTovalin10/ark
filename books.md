Here's the complete reading list with Raft and papers added:

---

# Reading List — Systems Engineering

Ordered by when to read, not importance. Each book is timed to land when you have the coursework to make it click.

---

## Right Now — Spring 2025

**1. Raft Paper — Ongaro & Ousterhout**
Read this weekend before anything else. Read it twice — first for understanding, second with annotations on Figure 2. Every rule in Figure 2 is a potential bug if you miss it. The extended version (Ongaro's dissertation Chapter 3) has more implementation detail than the conference paper — read both.

**2. Unix Network Programming Vol. 1 — W. Richard Stevens**
*Selected chapters: Part 1 (1–5), Part 2 (6–11), Chapter 16*
Read alongside your TCP implementation. You know the theory from Peterson & Davie — this gives you the POSIX API depth. Chapter 6 on I/O multiplexing is essential. Every sockets API question on your interview list is answered here.

---

## Summer at Truveta (June – August 2025)

**3. MapReduce Paper — Dean & Ghemawat**
Short read. Foundational distributed computing model. Read it in a weekend — the concepts appear constantly in distributed systems interviews even though nobody uses MapReduce directly anymore. Understand the programming model, fault tolerance, and why it was novel.

**4. Dynamo Paper — DeCandia et al. (Amazon)**
Read alongside your Raft Phase 1 and 2 work. Contrasts directly with Raft — eventual consistency vs strong consistency, quorum reads/writes, vector clocks, consistent hashing. Every AWS interview that touches distributed systems references Dynamo directly or indirectly. Understanding it deeply makes you a stronger AWS candidate specifically.

**5. CS:APP — Computer Systems: A Programmer's Perspective**
*Chapters 6, 8, 9, 10, 11, 12*
You have the OS theory from OSTEP. CS:APP gives you the lower-level hardware perspective that complements it and fills the gaps that show up in kernel interviews — cache hierarchy, signals, virtual memory, Unix I/O, network programming. Read it alongside your kernel patch work.

---

## Fall Senior Year (September – December 2025)

**6. Bigtable Paper — Chang et al. (Google)**
Read at the start of fall alongside 453. Covers distributed storage, SSTable format, LSM tree structure, and compaction. Directly relevant to 453 material and to storage system questions at GCP and Databricks. Understanding Bigtable makes Spanner make more sense.

**7. Spanner Paper — Corbett et al. (Google)**
Read mid-fall after Bigtable. The most important paper for GCP interviews specifically — external consistency, TrueTime, globally distributed transactions. GCP engineers built on or around Spanner. Knowing it signals genuine GCP interest beyond surface-level preparation.

**8. Chubby Paper — Burrows (Google)**
Read after Spanner. Chubby is Google's distributed lock service — it's essentially Paxos in production. Understanding how Google implemented consensus in practice, the lessons learned, and why they built Chubby instead of using Paxos directly gives you context for why etcd and Raft exist. Short and readable.

**9. Designing Data-Intensive Applications — Martin Kleppmann**
Read alongside 453. Perfect timing — the course and the book reinforce each other constantly. Go deep on chapters 5 (replication), 6 (partitioning), 7 (transactions), 8 (distributed systems problems), and 9 (consistency and consensus). This is the mental model you need for Raft Phase 3 sharding and for every distributed systems interview question.

**10. System Design Interview Vol. 1 — Alex Xu**
One weekend read, just for interview structure. Don't over-invest here — your actual systems knowledge is the substance. Xu gives you the format and the vocabulary interviewers expect. Internalize the framework: clarify requirements, estimate scale, high-level design, deep dive, wrap up.

---

## Winter (January – March 2026)

**11. Kafka Paper — Kreps et al. (LinkedIn)**
Short and readable. Log-structured distributed messaging — the concept of the commit log as a universal data structure is deeply relevant to your Raft work (Raft is fundamentally a replicated log). Understanding Kafka's design gives you vocabulary for stream processing questions at Databricks specifically.

**12. XDP Paper — Høiland-Jørgensen et al.**
Read as your kernel networking work deepens. XDP (eXpress Data Path) is how Cloudflare does high-performance packet processing. Understanding it technically — how it hooks into the kernel network stack before sk_buff allocation, why it's faster than normal processing, how it relates to eBPF — prepares you specifically for Cloudflare interviews.

**13. The Linux Programming Interface — Michael Kerrisk**
*Selected chapters: sockets (56–61), processes (24–28), signals (20–22), threads (29–33), epoll (63)*
The practical POSIX reference that goes deeper than UNP on Linux-specific behavior. Read this before interview season. Directly relevant to your kernel patch work and to systems programming questions at Cloudflare, AWS, and Red Hat.

**14. Site Reliability Engineering — Google**
*Chapters 1–4, 8, 13, 17*
Free at sre.google/books. Read before GCP applications open. Understand SLOs, error budgets, eliminating toil, and the operational philosophy. GCP interviewers will assume you've read it. Short chapters — a few hours total.

---

## Two Weeks Before Interviews (Spring 2026)

**15. WireGuard Paper — Donenfeld**
Short and elegant. Read before Cloudflare interviews specifically. WireGuard is a modern VPN protocol built on clean cryptographic principles — understanding its design philosophy and how it differs from OpenVPN/IPSec signals genuine networking depth. Cloudflare uses WireGuard internally.

**16. The Datacenter as a Computer — Barroso, Clidaras, Hölzle**
Free from Google. GCP context. Short read — a few hours. Gives you the mental model for how Google thinks about infrastructure at scale — warehouse-scale computing, tail latency, resource disaggregation, power efficiency. Signals genuine GCP interest in interviews.

**17. TCP/IP Illustrated Vol. 1 — W. Richard Stevens**
*TCP chapters only (17–24)*
Final deep TCP review for Cloudflare and AWS networking rounds. You know TCP from your networking course — this is the reference-level detail that separates candidates who understand it from candidates who've memorized it. Connection management, timeout and retransmission, congestion control at the packet trace level.

---

## Papers Summary Table

| Paper | When | Why |
|---|---|---|
| Raft (Ongaro) | Now | Before writing any Go |
| MapReduce (Dean) | Summer | Foundational, short |
| Dynamo (Amazon) | Summer | AWS interviews, eventual consistency |
| Bigtable (Google) | Fall | Storage systems, 453 context |
| Spanner (Google) | Fall | GCP interviews, external consistency |
| Chubby (Google) | Fall | Consensus in production |
| Kafka (LinkedIn) | Winter | Log-structured systems, Databricks |
| XDP | Winter | Cloudflare interviews, kernel networking |
| WireGuard | Pre-interview | Cloudflare specifically |

---

## Post-Graduation (While Working)

**BPF Performance Tools — Brendan Gregg**
eBPF and bpftrace reference. More useful once you're doing real kernel and infrastructure work than for interviews. Read the networking and CPU chapters when your job exposes you to performance analysis work.

**Systems Performance — Brendan Gregg**
Same timing — post-graduation. The methodology chapters are worth skimming before interviews but the depth is most valuable when you're diagnosing real production systems.

**TCP/IP Illustrated Vol. 2 — Stevens**
Implementation of the TCP/IP protocols in the BSD kernel. Read this when your kernel networking contributions go deep enough that you need implementation-level detail. Not needed for interviews — needed for becoming a serious kernel networking contributor.
