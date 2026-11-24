# Computer Science & Engineering Notes Hub: First Principles Knowledge Base

> Comprehensive master study guides, production-grade architectural diagrams, worked competitive/interview problems, and video transcripts distilled from foundational engineering curricula.

---

## 📖 Overview

This repository serves as a centralized, high-density knowledge base for core computer science disciplines and software engineering domains. Every subject is built strictly from first principles—bridging low-level hardware mechanics, operating system kernel abstractions, networking protocols, and modern distributed production systems.

### 📚 Available Subjects & Courses

| Subject / Course | Source Curriculum | Master Notes | Transcripts / Raw Material | Lectures / Scope |
| :--- | :--- | :---: | :---: | :---: |
| **Backend Engineering from First Principles** | *Backend from first principles* | [`COMPLETE_BACKEND_NOTES.md`](notes/backend-from-first-principles/COMPLETE_BACKEND_NOTES.md) &bull; [PDF Guide](notes/backend-from-first-principles/Backend_from_First_Principles_Notes.pdf) | [`transcripts/Backend from first principles/`](transcripts/Backend%20from%20first%20principles/) | 31 Chapters (Networking, Databases, Caching, Queues, Distributed Storage, DevOps) |
| **Operating Systems (Complete Course)** | *Knowledge Gate* (Sanchit Jain) &bull; [YouTube Playlist](https://www.youtube.com/playlist?list=PLxCzCOWd7aiGz9donHRrE9I3Mwn6XdP8p) | [`COMPLETE_OPERATING_SYSTEM_NOTES.md`](notes/operating-system/COMPLETE_OPERATING_SYSTEM_NOTES.md) | [`transcripts/Operating System (Complete Playlist)/`](transcripts/Operating%20System%20(Complete%20Playlist)/) | 92 Lectures (Kernel Architecture, CPU Scheduling, Concurrency, Deadlocks, Paging, Inodes) |

---

## 📂 Repository Structure

```
.
├── notes/
│   ├── backend-from-first-principles/
│   │   ├── COMPLETE_BACKEND_NOTES.md         # Master 31-Chapter backend guide (2,500+ lines, 57 diagrams)
│   │   └── Backend_from_First_Principles_Notes.pdf # Compiled master notes PDF
│   └── operating-system/
│       └── COMPLETE_OPERATING_SYSTEM_NOTES.md # Master 8-Module OS reference guide (Worked problems & formulas)
│
├── transcripts/
│   ├── Backend from first principles/        # 31 individual video transcripts + combined master file
│   └── Operating System (Complete Playlist)/  # 92 individual lecture transcripts + combined master file
│
├── get_playlist_transcripts.py               # Universal YouTube playlist transcript downloader & merger
├── requirements.txt                          # Dependencies (yt-dlp, youtube-transcript-api)
├── .gitignore                                # Environment, transcript caches, and Python ignores
└── README.md                                 # Central documentation hub
```

---

## 🖥️ Subject 1: Backend Engineering from First Principles

Master Guide: [`notes/backend-from-first-principles/COMPLETE_BACKEND_NOTES.md`](notes/backend-from-first-principles/COMPLETE_BACKEND_NOTES.md)

### Curriculum Outline (8 Modules &bull; 31 Chapters)

#### Module 1: Foundations, Architecture & The HTTP Protocol
- **Chapter 01 (Video 001):** The 28 Architectural Pillars of Modern Backend Systems
- **Chapter 02 (Video 002):** Mindset & The 3 Learning Phases (Philosophy → Polyglot Code → Production Systems)
- **Chapter 03 (Video 003):** Physical Request Flow (DNS → Security Group → Nginx → Node/PM2 → DB), State Centralization, and Why Frontends Cannot Be Backends
- **Chapter 04 (Video 004):** The ROI of Learning Backend Engineering from First Principles
- **Chapter 05 (Video 005):** Deep Dive into HTTP (L4 TCP vs L7 HTTP, HTTP/1.0 through HTTP/3 QUIC, Head-of-Line Blocking, Headers, Methods & Idempotency, CORS Preflight Flow, Status Codes, Caching & ETags)

#### Module 2: Core Web API Mechanics & Application Architecture
- **Chapter 06 (Video 006):** Routing Tables `(METHOD, PATH)`, Dynamic Segments, Query vs Path Parameters, Nesting, and API Versioning
- **Chapter 07 (Video 007):** Serialization & Deserialization across Heterogeneous Runtimes, Text (JSON/XML) vs Binary (Protobuf), and JSON Grammar Limits
- **Chapter 08 (Video 008):** AuthN vs AuthZ, Historical Evolution, Stateful Sessions vs Stateless JWTs, Cookies (`HttpOnly`, `Secure`, `SameSite`), OAuth 2.0 / OIDC Delegation, RBAC/ABAC/ReBAC, User Enumeration & Timing Attacks
- **Chapter 09 (Video 009):** Boundary Defense, Fail-Fast Principle, Syntactic/Semantic/Type Validation, and Data Normalization
- **Chapter 10 (Video 010):** Layered Architecture (Controllers vs Services vs Repositories), Middleware Pipeline Order, and Request Context
- **Chapter 11 (Video 011):** Roy Fielding's 6 REST Constraints, URI Modeling, Offset vs Cursor/Keyset Pagination, and Standardized Envelopes

#### Module 3: Persistence, Caching & Search Engine Architecture
- **Chapter 12 (Video 012):** PostgreSQL Architecture, Flat File Limitations, Data Types (`TEXT` vs `VARCHAR`, `NUMERIC` vs `FLOAT`, `TIMESTAMPTZ`, UUIDs, `JSON` vs `JSONB`), Constraints, Migrations, Soft Deletes, and B-Tree Indexing (`EXPLAIN ANALYZE`)
- **Chapter 13 (Video 013):** Memory Hierarchy, Caching Layers, Cache-Aside vs Write-Through vs Write-Back, Eviction (LRU/LFU/TTL), Cache Stampede/Thundering Herd (Mutexes, XFetch), and Cache Penetration (Bloom Filters)
- **Chapter 14 (Video 015):** Why SQL `ILIKE` Fails, Inverted Index Internals, Analysis Pipelines (Tokenizers, Stemming, Stop Words), `text` vs `keyword`, and BM25 Relevance Scoring

#### Module 4: Asynchronous Processing, Real-Time & Event-Driven Systems
- **Chapter 15 (Video 014):** Synchronous Latency Traps, Task Queue Architecture (Producers, Brokers, Consumers), Priority Queues, DAG Workflows, Exponential Backoff with Jitter, Dead Letter Queues (DLQ), and Worker Idempotency
- **Chapter 16 (Video 026):** Polling vs SSE vs WebSockets, Handshake Protocol (`101 Switching Protocols`), Linux File Descriptors (`ulimit -n`), and Cross-Instance Scaling with Redis Pub/Sub
- **Chapter 17 (Video 030):** Webhooks as Reverse APIs, HMAC-SHA256 Signatures, Raw Body Verification, Constant-Time Comparison, Replay Defenses, and Provider SSRF Safeguards

#### Module 5: Scalable Object Storage & Unstructured Data
- **Chapter 18 (Video 024):** Object Storage Flat Namespace, Availability vs 11 9s Durability, and Direct Pre-signed `PUT` URLs
- **Chapter 19 (Video 025):** Multipart Upload Protocol (Initiation → Parallel 5–10MB Chunk Uploads → Complete Assembly), Lifecycle Auto-Abort Rules, Pre-signed `GET` URLs, and CDN Edge Delivery

#### Module 6: Resilience, Configuration & Observability
- **Chapter 20 (Video 016):** Error Taxonomy (Programmer vs Operational vs Client), Fail-Fast Boot, Centralized Error Middleware, Information Disclosure Sanitization, Timeouts, and Circuit Breakers
- **Chapter 21 (Video 017):** 12-Factor Config (Factor III), `.env` vs `.env.example`, Cloud Secrets Managers, and Boot Schema Validation
- **Chapter 22 (Video 018):** Logs vs Metrics vs Traces, Structured JSON Logging, Log Levels, PII Masking, Latency Percentiles (p50, p95, p99), and OpenTelemetry
- **Chapter 23 (Video 019):** Catastrophic Abrupt Kills vs Graceful Shutdown, POSIX Signals (`SIGINT`, `SIGTERM`, `SIGKILL`), In-Flight Request Draining, Connection Pool Teardowns, and Timeout Safeguards

#### Module 7: Security Engineering & High-Performance Scaling
- **Chapter 24 (Video 020):** Defense in Depth, SQL Injection, Slow Password Hashing (Argon2id/bcrypt with Salt & Cost Factors), BOLA/IDOR Tenant Scoping, XSS, CSRF, and Security Headers
- **Chapter 25 (Video 021):** Latency vs Throughput, CPU Flame Graphs, Profiling before Optimizing, Missing Indexes, N+1 Query Batching, and Connection Pool Sizing
- **Chapter 26 (Video 022):** Vertical vs Horizontal Scaling, L4 vs L7 Load Balancers, Read Replicas, WAL Streaming Replication, and Read-Your-Own-Writes Consistency
- **Chapter 27 (Video 023):** Concurrency vs Parallelism, I/O-Bound vs CPU-Bound Profiles, OS Threads vs Event Loop vs Goroutines (2 KB Stack & M:N Scheduler), Race Conditions, Mutexes, and Deadlocks

#### Module 8: Quality Engineering, Cloud-Native Standards & DevOps
- **Chapter 28 (Video 027):** Testing Pyramid, Test Doubles (Dummies, Stubs, Spies, Mocks, Fakes), Testcontainers for Real DBs, TDD (Red-Green-Refactor), Flaky Test Quarantine, and Cyclomatic Complexity (≤ 10)
- **Chapter 29 (Video 028):** Exhaustive Breakdown of All Twelve Factors in the 12-Factor App Methodology
- **Chapter 30 (Video 029):** OpenAPI 3.x Specifications, Design-First Workflows, Mock Servers (Prism), and Automated SDK Generation
- **Chapter 31 (Video 031):** DevOps for Backends, CI/CD, Linux Namespaces & Cgroups, Multi-Stage Distroless Dockerfiles, Kubernetes Primitives (Pods, Deployments, Services), Zero-Downtime Deployments, and Blameless Post-Mortems

---

## ⚙️ Subject 2: Operating Systems (Complete Academic & Systems Guide)

Master Guide: [`notes/operating-system/COMPLETE_OPERATING_SYSTEM_NOTES.md`](notes/operating-system/COMPLETE_OPERATING_SYSTEM_NOTES.md)  
Source: [Knowledge Gate - Sanchit Jain OS Playlist](https://www.youtube.com/playlist?list=PLxCzCOWd7aiGz9donHRrE9I3Mwn6XdP8p) (92 Lectures)

### Curriculum Outline (8 Modules &bull; 92 Lectures)

#### Module 1: OS Fundamentals, Architecture, Process Lifecycle & System Calls (Lec 0 – 1.12)
- Hardware abstractions, OS goals (Convenience vs Throughput), Kernel vs Shell.
- OS Classifications: Batch systems, Multiprogramming, Time-sharing (Multitasking), Hard/Soft RTOS, Distributed & Clustered systems.
- 5-State and 7-State Process lifecycle; Schedulers (Long-Term, Short-Term, Medium-Term Swapper) and Dispatcher latency.
- Essential Linux diagnostics: `ps`, `top`, `vmstat`, `ipcs`, `nice`, `renice`, `strace`.
- Dual-Mode operation: User Mode (Ring 3) vs Kernel Mode (Ring 0), mode bit, privileged instructions, trap vectors.
- `fork()` system call: Copy-on-Write (COW), process hierarchy trees ($2^n - 1$ children), Zombie vs Orphan processes.
- Threads: Process vs Thread control blocks, User-Level Threads (ULT) vs Kernel-Level Threads (KLT), 1:1, M:1, and M:N mapping.

#### Module 2: CPU Scheduling Algorithms & Multiprogramming Metrics (Lec 2.1 – 2.11)
- Preemption vs Non-preemption decision criteria; metrics: Arrival Time ($AT$), Burst Time ($BT$), Completion Time ($CT$), Turnaround Time ($TAT = CT - AT$), Waiting Time ($WT = TAT - BT$), Response Time ($RT$).
- First-Come First-Served (FCFS) & Convoy effect analysis.
- Shortest Job First (SJF) & Shortest Remaining Time First (SRTF) worked problems.
- Round Robin (RR) with Time Quantum calibration and context switch overhead.
- Priority scheduling, Starvation, and Aging mitigation.
- Mixed CPU and I/O burst multi-job scheduling.
- Multi-Level Queue (MLQ) and Multi-Level Feedback Queue (MLFQ).

#### Module 3: Process Synchronization, Critical Sections & Semaphores (Lec 3.1 – 3.13)
- Race conditions and shared state corruption.
- Critical Section Problem: 3 mandatory criteria (Mutual Exclusion, Progress, Bounded Waiting).
- Synchronization pitfalls: Producer-Consumer (bounded buffer), Printer-Spooler race condition.
- Software & Hardware locks: Lock variable flaws, Turn variable (strict alternation), Peterson’s two-process algorithm, atomic `Test-and-Set`.
- Counting & Binary Semaphores (Dijkstra): `wait()` / `P()` and `signal()` / `V()` operations.
- Classical Concurrency Problems solved: Producer-Consumer, Reader-Writer (reader preference), Dining Philosophers.

#### Module 4: Deadlocks: Characterization, Graphs, Prevention & Avoidance (Lec 4.1 – 4.8)
- Deadlock definition and distinction from starvation.
- 4 Coffman Conditions: Mutual Exclusion, Hold and Wait, No Preemption, Circular Wait.
- Resource Allocation Graphs (RAG): Cycle detection in Single-Instance vs Multi-Instance resources.
- Handling Strategies: Ostrich algorithm (Deadlock ignorance), Deadlock prevention (invalidating Coffman conditions).
- Deadlock Avoidance: Banker’s Algorithm (Allocation, Max, Available, Need matrix, Safety algorithm sequence check, Resource-Request verification).

#### Module 5: Memory Management, Paging, Virtual Memory & Page Replacement (Lec 5.1 – 5.26, Lec 90)
- Contiguous Memory Allocation: Fixed vs Dynamic partitioning, Internal vs External fragmentation, Compaction.
- Dynamic Allocation Policies: First Fit, Next Fit, Best Fit, Worst Fit.
- Non-Contiguous Allocation: Paging architecture, Logical to Physical Address Space mapping, MMU translation.
- Page Table Entry format (Frame, Valid/Invalid, Dirty, Reference, Protection bits).
- Multilevel Paging address decomposition and memory overhead calculations.
- Inverted Page Tables, Segmentation vs Paging, Thrashing (Working Set Model).
- Virtual Memory & Demand Paging: Page Fault Service Routine (PFSR), Effective Memory Access Time (EMAT).
- Translation Lookaside Buffer (TLB): Hit ratio ($\alpha$) and multi-tier access latency formulas.
- Page Replacement Algorithms: FIFO (Belady’s Anomaly), Optimal (MIN), LRU, and MRU.

#### Module 6: Secondary Storage Structure & Disk Scheduling (Lec 6.1 – 6.10)
- Magnetic hard disk geometry: Platters, Tracks, Cylinders, Sectors, Read/Write heads.
- Disk Access Time: Seek Time, Rotational Latency, Transfer Time, Controller Overhead.
- Disk Scheduling Algorithms with cylinder head movement calculations: FCFS, SSTF, SCAN (Elevator), LOOK, C-SCAN, C-LOOK.

#### Module 7: File Systems Organization, Allocation & Unix Inode (Lec 7.1 – 7.7)
- File attributes, operations, file directory organizations.
- File Allocation Methods: Contiguous, Linked List, Indexed Allocation.
- Unix Inode Structure: Direct block pointers, Single Indirect, Double Indirect, Triple Indirect addressing.
- Maximum file capacity calculation given block size and pointer width.

#### Module 8: System Protection, Security, Program Lifecycle & Placement Q&A (Lec 8, 90, 91, 92)
- Protection vs Security, Access Matrix model, Access Control Lists (ACL) vs Capability Lists.
- Program Lifecycle: Compiler $\to$ Assembler $\to$ Linker (Symbol resolution, Static vs Dynamic linking) $\to$ Loader (`execve`, memory allocation).
- High-yield placement and GATE competitive exam technical interview Q&A.

---

## 🛠️ Tooling: Automated YouTube Playlist Transcript Downloader

The included CLI utility [`get_playlist_transcripts.py`](get_playlist_transcripts.py) automatically extracts, formats, and combines video-by-video transcripts for any YouTube playlist.

### 1. Environment Setup

```bash
# Clone the repository
git clone https://github.com/AkhandPratapSingh11/backend-from-first-principles.git notes-knowledge-base
cd notes-knowledge-base

# Create and activate Python virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install required dependencies
pip install -r requirements.txt
```

### 2. Usage Examples

```bash
# Download transcripts for the Operating System playlist
python get_playlist_transcripts.py "https://www.youtube.com/playlist?list=PLxCzCOWd7aiGz9donHRrE9I3Mwn6XdP8p" \
  -o "./transcripts" \
  -l en hi en-US en-GB \
  --combine

# Download transcripts for the Backend from first principles playlist
python get_playlist_transcripts.py "https://www.youtube.com/playlist?list=PLui3EUkuMTPgZcV0QhQrOcwMPcBCcd_Q1" \
  -o "./transcripts" \
  --combine

# Save raw structured JSON alongside formatted text transcripts
python get_playlist_transcripts.py <PLAYLIST_URL> --json --combine

# Extract only the first 10 lectures without timestamps
python get_playlist_transcripts.py <PLAYLIST_URL> --limit 10 --no-timestamps
```

### Output Format
For any processed playlist, the tool generates:
1. Individual timestamped lecture transcripts: `001_Lecture_Title_VideoID.txt`
2. Merged single master study transcript: `000_ALL_TRANSCRIPTS_COMBINED.txt`

---

## 🤝 Contributing

Contributions to notes, clarifications, diagrams, and additional course transcripts are welcome:
1. Fork this repository.
2. Create a new topical branch (`git checkout -b topic/new-course-notes`).
3. Add or update notes in `notes/<subject-name>/`.
4. Commit your changes (`git commit -m "Add notes for XYZ"`).
5. Push to your branch and open a Pull Request.

---

## 📜 License

This repository is maintained for educational and non-commercial engineering reference. Course video content and original lecture materials belong to their respective creators.
