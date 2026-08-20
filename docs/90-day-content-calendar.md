# 90-Day LinkedIn Content Calendar

**Brand:** Mujtaba Bukhari — Backend-Focused Full Stack Developer  
**Positioning:** *How real production systems work* (not framework syntax 101)  
**Audience:** Senior engineers, EMs, founders, recruiters, ambitious mid-levels  
**Cadence:** Daily · LinkedIn · caption + template graphic  
**Voice:** Builder journal + teacher · tradeoffs, failure modes, design decisions  

**Stack signal:** Node.js · Koa.js · TypeScript · MySQL · ClickHouse · Redis · React · multi-tenant SaaS (ATS)

---

## Content pillars (recurring series)

| Series | What it does |
|--------|----------------|
| **System Design Simplified** | Real architectures: gateway, notifications, chat, uploads, feeds, booking-style systems |
| **Production Lessons** | Bugs, outages, debugging order, incidents, “only in prod” stories |
| **Backend Deep Dives** | Internals: bcrypt/JWT/HTTPS/DNS/event loop — *how it works*, not *what is* |
| **Database Mastery** | Indexes, locking, isolation, replicas, plans, pooling, ClickHouse vs OLTP |
| **Building SaaS at Scale** | Multi-tenant, RBAC, permissions, auth flows, APIs, caching in enterprise apps |
| **Security Engineering** | Authn/z, webhooks, SSRF, secrets, safer APIs |
| **Distributed Systems** | Queues, idempotency, saga, locks, consistency |
| **AI for Backend Engineers** | RAG, embeddings, rate limits, function calling, cost/safety |
| **Engineering Mindset** | Decisions, debt, simplicity, contracts, reviews |
| **Frontend for Backend Engineers** | React Query, optimistic UI, e2e auth, uploads |

**Level mix:** ~80% production / architecture / internals · ~20% important foundations (kept on purpose — Day 1 Salt vs Pepper is the model).

---

## How we run this

1. Pick the day’s row  
2. Fill the assigned **template**  
3. Deliver caption + graphic same day  
4. Status: `pending` → `ready` → `posted`

| Status | Meaning |
|--------|---------|
| pending | not started |
| ready | caption + graphic in `posts/` |
| posted | live on LinkedIn |

**Progress:** Days 1–9 **posted**. Day 10 **ready**. Next: **Day 11**.

---

## Calendar

| Day | Topic | Hook | Series | Template | Status |
|-----|-------|------|--------|----------|--------|
| 1 | Salt vs Pepper | Most developers confuse Salt and Pepper… | Backend Deep Dives | Compare | posted |
| 2 | Access + Refresh Tokens | Short-lived proof vs long-lived renewer — get lifetime wrong and security breaks. | Security Engineering | Compare | posted |
| 3 | Refresh Token Rotation | A stolen refresh token shouldn't own the account forever. | Security Engineering | How-it-works | posted |
| 4 | JWT Revocation at Scale | Stateless JWTs get painful the day you need instant logout. | Security Engineering | Mistake vs Fix | posted |
| 5 | How JWT Signatures Work | A JWT isn't encrypted by default — it's signed. That difference matters. | Backend Deep Dives | How-it-works | posted |
| 6 | OAuth vs OpenID Connect | OAuth authorizes access. OIDC answers *who* the user is. | Security Engineering | Compare | posted |
| 7 | API Gateway Architecture | Large companies don't expose microservices directly — and neither should you past a point. | System Design Simplified | How-it-works | posted |
| 8 | What is Rate Limiting | Rate limiting protects your API before traffic becomes a problem. | System Design Simplified | How-it-works | posted |
| 9 | Rate Limiting Algorithms | Fixed-window limits lie under burst traffic. | System Design Simplified | Compare | posted |
| 10 | Idempotency Keys | Retries are normal. Duplicate charges and duplicate jobs shouldn't be. | Distributed Systems | How-it-works | ready |
| 11 | Webhook HMAC + Replay | Signature checks without timestamp/nonce checks still get replayed. | Security Engineering | Code tip | pending |
| 12 | Notification System Design | Email/SMS/push aren't “send and forget” — they're queues, retries, and DLQs. | System Design Simplified | How-it-works | pending |
| 13 | Dead Letter Queues | Infinite retries without a DLQ turn outages into infinite cost. | Distributed Systems | How-it-works | pending |
| 14 | File Upload Architecture | Streaming uploads through your Node API is how you invent timeouts. | System Design Simplified | How-it-works | pending |
| 15 | Pre-signed URLs | A public bucket with obscure URLs is not authorization. | System Design Simplified | Mistake vs Fix | pending |
| 16 | Multi-Tenant SaaS Isolation | One missing `tenantId` in a WHERE clause is a breach, not a bug. | Building SaaS at Scale | Mistake vs Fix | pending |
| 17 | Shared vs Separate DB Tenancy | Shared DB is cheaper. Separate DB is cleaner. The tradeoff is operational, not moral. | Building SaaS at Scale | Compare | pending |
| 18 | RBAC vs ReBAC | Role explosion is the tax for oversimplified permissions. | Building SaaS at Scale | Compare | pending |
| 19 | Permission Systems in Hiring SaaS | “Who can create a job” is a business transaction — ATR, approvals, audit. | Building SaaS at Scale | Builder journal | pending |
| 20 | bcrypt Internals | bcrypt stores the salt in the hash string — here's what those `$` sections mean. | Backend Deep Dives | How-it-works | pending |
| 21 | HTTPS / TLS Handshake | Your API is reachable before it's trustworthy — TLS is the negotiation. | Backend Deep Dives | How-it-works | pending |
| 22 | DNS Before the First Byte | Latency starts before your Koa handler runs. | Backend Deep Dives | How-it-works | pending |
| 23 | Node.js Event Loop Internals | `await` doesn't mean “other work can't starve” — phases still matter. | Backend Deep Dives | How-it-works | pending |
| 24 | TCP vs HTTP | HTTP problems are often TCP problems wearing a nicer status code. | Backend Deep Dives | Compare | pending |
| 25 | REST vs RPC | Resource modeling vs procedure calls — pick for the contract, not the hype. | Backend Deep Dives | Compare | pending |
| 26 | How GraphQL Executes Queries | Resolvers + N+1 is how a “flexible API” becomes a database thrasher. | Backend Deep Dives | Mistake vs Fix | pending |
| 27 | Why Indexes Are Fast | Indexes aren't magic — they're data structures that avoid scanning rows. | Database Mastery | How-it-works | pending |
| 28 | Composite Indexes | Leftmost prefix rules will silently ignore the index you “added.” | Database Mastery | Mistake vs Fix | pending |
| 29 | Covering Indexes | The fastest query never touches the base table. | Database Mastery | Code tip | pending |
| 30 | Clustered vs Non-Clustered | InnoDB already clustered your PK — secondary indexes pay a lookup tax. | Database Mastery | Compare | pending |
| 31 | Normalize vs Denormalize | Normalize for writes. Denormalize for the query you run 10M times. | Database Mastery | Compare | pending |
| 32 | Partitioning | Partitioning isn't sharding — but bad partition keys create the same pain. | Database Mastery | How-it-works | pending |
| 33 | Replication & Read Replicas | Replica lag turns “eventually consistent” into “wrong UI for 3 seconds.” | Database Mastery | Builder journal | pending |
| 34 | Sharding Reality Check | Sharding multiplies ops cost before it multiplies capacity. | Database Mastery | Mistake vs Fix | pending |
| 35 | Transactions & Partial Failure | Saving half the write is worse than saving none. | Database Mastery | How-it-works | pending |
| 36 | Deadlocks | Deadlocks aren't random — lock order is. | Database Mastery | Mistake vs Fix | pending |
| 37 | Optimistic vs Pessimistic Locking | `SELECT FOR UPDATE` everywhere will serialize your throughput. | Database Mastery | Compare | pending |
| 38 | Isolation Levels | READ COMMITTED still allows anomalies finance flows can't tolerate. | Database Mastery | Compare | pending |
| 39 | Connection Pool Exhaustion | The API isn't slow — every request is waiting for a free connection. | Production Lessons | How-it-works | pending |
| 40 | EXPLAIN ANALYZE | Estimated rows lying to you is how “optimized” queries still timeout. | Database Mastery | How-it-works | pending |
| 41 | Slow Query Optimization | Measure the plan, then the index, then the query shape — in that order. | Database Mastery | Builder journal | pending |
| 42 | OLTP MySQL vs ClickHouse | MySQL isn't slow — you're forcing OLTP to do analytics. | Database Mastery | Compare | pending |
| 43 | Cache Stampede | One hot key expiry can DDoS your own database. | Production Lessons | How-it-works | pending |
| 44 | Caching Strategies | TTL-only caches are how permissions stay wrong for 10 minutes. | Building SaaS at Scale | Compare | pending |
| 45 | Redis Distributed Locks | A lock without fencing tokens is a race with confidence. | Distributed Systems | Mistake vs Fix | pending |
| 46 | Message Queues in Practice | At-least-once delivery means your consumer must be idempotent. | Distributed Systems | How-it-works | pending |
| 47 | Kafka vs RabbitMQ (Engineer View) | Log stream vs smart broker — choose the failure model, not the logo. | Distributed Systems | Compare | pending |
| 48 | Saga Pattern | Distributed “transactions” are compensation, not ACID. | Distributed Systems | How-it-works | pending |
| 49 | CQRS When It Pays Off | Separate read models only when query shape fights write model. | Distributed Systems | Builder journal | pending |
| 50 | Event Sourcing Tradeoffs | Perfect audit trail, harder refactors — know why you're paying. | Distributed Systems | Compare | pending |
| 51 | CAP Theorem in Product Terms | You're always picking which users see which wrongness under partition. | Distributed Systems | Code tip | pending |
| 52 | Eventual Consistency UX | The hard part isn't the database — it's what the UI promises. | Distributed Systems | Mistake vs Fix | pending |
| 53 | Leader Election Basics | Someone has to own the cron, the lock, or the partition. | Distributed Systems | How-it-works | pending |
| 54 | Race Conditions Only in Prod | Local single-instance testing hides the bug your three replicas create. | Production Lessons | Builder journal | pending |
| 55 | When Logs Aren't Enough | Metrics → traces → logs → SSH — not the reverse. | Production Lessons | How-it-works | pending |
| 56 | N+1 in Production | Your ORM didn't write 200 queries — your access pattern did. | Production Lessons | Mistake vs Fix | pending |
| 57 | API Latency Analysis | p99 hides in dependency waterfalls, not in your handler's happy path. | Production Lessons | How-it-works | pending |
| 58 | Background Job Retries | Retry without backoff and idempotency is a self-inflicted outage. | Production Lessons | Mistake vs Fix | pending |
| 59 | Circuit Breakers | Calling a dying dependency harder is how cascades start. | Production Lessons | How-it-works | pending |
| 60 | Graceful Shutdown | Ignoring SIGTERM drops in-flight requests on every deploy. | Production Lessons | Code tip | pending |
| 61 | Memory Leaks from Unclosed Resources | The leak is often a Map, a listener, or a pool — not “Node being Node.” | Production Lessons | Builder journal | pending |
| 62 | Chat System Architecture | WebSockets + presence + fanout is an architecture problem, not a library choice. | System Design Simplified | How-it-works | pending |
| 63 | Presence, Typing, Read Receipts | Ephemeral state belongs in memory/Redis — not your primary OLTP tables. | System Design Simplified | Code tip | pending |
| 64 | URL Shortener Design | Short codes, collisions, redirects, and analytics — small product, real scale lessons. | System Design Simplified | How-it-works | pending |
| 65 | Feed / Timeline Architecture | Fan-out on write vs read — LinkedIn-style feeds are caching + ranking decisions. | System Design Simplified | Compare | pending |
| 66 | Cursor Pagination + Infinite Scroll | Offset pagination quietly dies as the feed grows. | System Design Simplified | Compare | pending |
| 67 | Ride-Booking Style Matching | Geo indexes + realtime updates — nearby matching under load. | System Design Simplified | How-it-works | pending |
| 68 | Reverse Proxy & Nginx | Your Node process shouldn't be the public edge. | System Design Simplified | How-it-works | pending |
| 69 | Load Balancers & Health Checks | Bad health checks remove healthy nodes — or keep dead ones in rotation. | System Design Simplified | Mistake vs Fix | pending |
| 70 | CDN from an API Dev View | Static isn't the only thing CDNs change — cache headers are part of your contract. | System Design Simplified | Code tip | pending |
| 71 | Docker Internals (App Dev Lens) | Namespaces and cgroups explain more outages than “restart the container.” | System Design Simplified | How-it-works | pending |
| 72 | Containers vs VMs | Isolation boundaries differ — so do noisy-neighbor and security assumptions. | System Design Simplified | Compare | pending |
| 73 | K8s Basics for Backend Devs | Pods, probes, and rolling deploys — what actually keeps traffic flowing. | System Design Simplified | How-it-works | pending |
| 74 | Auto Scaling Pitfalls | Scaling replicas won't help if the bottleneck is a single DB writer. | Production Lessons | Mistake vs Fix | pending |
| 75 | API Security Checklist | Authn, authz, input, rate limits, SSRF — the list that survives review. | Security Engineering | Code tip | pending |
| 76 | CSRF, XSS, SSRF (Backend Angle) | Browser trust boundaries show up in your cookies, redirects, and fetch calls. | Security Engineering | Compare | pending |
| 77 | Password Reset Vulnerabilities | Most reset flows fail on token storage, expiry, or user enumeration. | Security Engineering | Mistake vs Fix | pending |
| 78 | Secrets Management | Hardcoded secrets aren't the only smell — never-rotated ones are. | Security Engineering | Mistake vs Fix | pending |
| 79 | Encryption at Rest vs In Transit | TLS doesn't encrypt your database backups. | Security Engineering | Compare | pending |
| 80 | Adding AI to a SaaS Product | AI is a dependency with cost, latency, and failure modes — design it like one. | AI for Backend Engineers | Builder journal | pending |
| 81 | Embeddings + Vector DBs | Search isn't LIKE anymore — but vectors need the same prod discipline. | AI for Backend Engineers | How-it-works | pending |
| 82 | RAG Architecture | Retrieval quality beats prompt cleverness when answers must be grounded. | AI for Backend Engineers | How-it-works | pending |
| 83 | AI Rate Limits & Caching | Token spend and vendor 429s need idempotency and cache layers too. | AI for Backend Engineers | Code tip | pending |
| 84 | Function Calling / Tool Use | Letting models call tools means authz checks on every tool path. | AI for Backend Engineers | Mistake vs Fix | pending |
| 85 | React Query & API Performance | Local state for server data invents cache bugs your backend already solved. | Frontend for Backend Engineers | Compare | pending |
| 86 | Optimistic UI + Rollback | Optimistic updates without conflict rules create confident lies. | Frontend for Backend Engineers | How-it-works | pending |
| 87 | Auth Flow End-to-End | Cookie/Bearer choices must agree across SPA, API, and gateway. | Frontend for Backend Engineers | How-it-works | pending |
| 88 | Case Study: Job Posting API | Problem → constraints → design → tradeoffs (anonymized SaaS). | Building SaaS at Scale | Builder journal | pending |
| 89 | Case Study: Permission System | How approval workflows change your data model more than your UI does. | Building SaaS at Scale | Builder journal | pending |
| 90 | Engineering Mindset + Reflection | Production sense compounds faster than syntax. 90 days of shipping in public. | Engineering Mindset | Builder journal | pending |

---

## Arc (feed narrative)

| Days | Focus |
|------|--------|
| 1–6 | Auth foundations + deep dives (kept basics that still matter) |
| 7–18 | Gateways, notifications, uploads, multi-tenant SaaS |
| 19–25 | Backend internals (HTTPS, DNS, event loop, GraphQL execution) |
| 26–41 | Database mastery + ClickHouse |
| 42–52 | Caching, queues, distributed patterns |
| 53–60 | Production lessons / incident-ready engineering |
| 61–73 | System design classics + infra from an app-dev lens |
| 74–78 | Security engineering |
| 79–83 | AI for backend engineers |
| 84–86 | Frontend bridge |
| 87–90 | Case studies + positioning |

---

## Important basics we kept (on purpose)

These stay because seniors still misuse them and juniors need the correct mental model:

- Salt vs Pepper (Day 1 — posted)  
- Access / refresh tokens (Day 2)  
- bcrypt internals (Day 19)  
- Why indexes are fast (Day 26)  
- Transactions / isolation (Days 34, 37)  
- CSRF/XSS/SSRF overview (Day 75)  

Everything else is framed as **production systems, architecture, and failure modes**.

---

## Notes

- Hooks are openers; captions expand with one diagram-worthy mechanism + tradeoff + CTA.  
- Sanitize Occy/client details in case studies; speak in patterns.  
- Bonus evergreen outside the 90: `posts/2026-08-05` Access vs Refresh (optional; Day 2 covers related ground — don't double-post same week).  
- **Next deliverable:** Day 2 — Access + Refresh Tokens (Compare template + graphic + caption).
