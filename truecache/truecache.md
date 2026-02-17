# Introduction

## About Oracle True Cache

Oracle True Cache is a built-in, in-memory caching service that runs inside the Oracle AI Database, eliminating the need for external cache systems such as Redis or Memcached. Unlike traditional mid-tier caches that introduce stale data risks and operational complexity, True Cache stays transactionally consistent with the underlying database through Oracle's proven redo technology, the same mechanism that powers Data Guard. Applications get microsecond read latency with zero code changes, while writes continue flowing to the authoritative primary database for full durability.

**The Challenge**: High-traffic applications suffer from slow database round-trips on repeated reads, yet every traditional caching solution introduces its own set of problems: stale data, manual invalidation logic, separate skill sets, and security gaps. Developers are forced to choose between performance and consistency, but they should not have to.

**What if your cache was always guaranteed to be correct?**

## The Solution: Oracle True Cache

**Oracle True Cache** is a **built-in caching service** that runs inside the Oracle AI Database, delivering ultra-low latency reads without ever serving stale data.

### How It Works:
- **Reads** are served directly from True Cache memory at microsecond speed
- **Writes** go to the primary Oracle AI Database for durability and consistency
- **Redo synchronisation** propagates every committed change from the primary to True Cache automatically - no manual invalidation, no TTL tuning

### Key Capabilities:
- Automatic data synchronisation using Oracle AI Database redo technology
- No application changes required, works transparently with existing SQL queries
- Ultra-low latency reads: microsecond-level response times from memory
- No data stored on disk by default, qualifies as a data-processing tier under data residency regulations
- Optionally overflow to disk when memory is full, still faster than the back-end database

### **Try the Interactive Demo**
Note: You can minimize the menu by clicking '≡' to better interact with the demo.

<iframe src="truecache.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>

###  
### 

### What You'll Discover:

- **The Problem**: Visualize how every read request travels all the way to the back-end database, creating latency bottlenecks and CPU exhaustion at high traffic volumes.

- **Cache Pitfalls**: See how traditional mid-tier caches (Redis, Memcached, object caches) create a dangerous tradeoff, fast reads but stale data. Watch the write path bypass the cache entirely while the cache continues serving outdated values.

- **True Cache Introduced**: Experience the three-node architecture - Application, True Cache, and Primary DB, where reads are intercepted by True Cache at microsecond speed while writes still flow to the authoritative source.

- **Always Fresh Data**: Watch Oracle's redo technology in action. Every commit on the primary instantly propagates to True Cache via the golden redo stream, ensuring applications always receive correct, up-to-date data without any application-side invalidation logic.

- **Scale Out**: Discover how multiple True Cache instances can be deployed simultaneously, each receiving the same redo stream to serve different teams (HR, Sales, Finance) with their own warmed data sets and to aggregate memory capacity for larger working sets.

- **Go Closer**: See how True Cache can be deployed geographically near the application in the same region, edge location, or data centre, serving reads locally at microsecond speed while the authoritative primary database remains centralised.

- **Business Value**: Explore real customer workloads running on True Cache today, from stock exchange ticker feeds to fraud detection AI inferencing to core banking offload.

## What Is Oracle True Cache?

A **built-in caching service** that runs inside the Oracle AI Database, eliminating the need for external cache systems.

### Core Properties:

**Automatic data synchronisation:**
Keeps cached data transactionally consistent with the underlying database, so applications always read fresh, correct data. Synchronisation uses Oracle AI Database redo technology, the same proven mechanism behind Data Guard, ensuring automatic refresh with no manual invalidation and consistency maintained across everything related to cached data.

**No application changes required:**
Works transparently with existing SQL queries and applications. There is no API to learn, no client library to install, and no query rewriting needed.

**Ultra-low latency reads:**
Delivers microsecond-level response times by serving frequently accessed data directly from memory. Reads that previously required a full database round-trip are served locally, dramatically reducing response times for read-heavy workloads.

**Writes go to the primary:**
All write operations continue to flow to the primary Oracle AI Database, preserving full ACID guarantees and durability. True Cache is a read offload tier, not a write-through cache.

## Why Mid-Tier Caches Fall Short

High-end applications often configure mid-tier caches to improve response times and reduce back-end database load. Whether the cache delivers positive results depends on several hard questions that are rarely answered satisfactorily:

- **Are you sure the data in the cache is up to date?** If not, what do you do?
- **How do you determine what data to cache?** Choosing the right objects requires deep domain knowledge and continuous tuning.
- **What specific technology is used?** Redis, Memcached, and custom object caches each have different semantics, consistency models, and operational profiles.
- **Who owns the invalidation logic?** Every write path in the application must be audited and updated to keep the cache coherent.
- **What about security?** Data that leaves the Oracle Database loses the security controls, auditing, and encryption that come with it.

Many of these questions make mid-tier caches deliver very limited positive results in practice and carry real business risk when stale data reaches end users.

**True Cache eliminates all of these concerns** by making the cache an integral, consistent part of Oracle AI Database itself.

## The Most Important Cache Requirement: Keeping Data Current

The single most important property of any cache is correctness. True Cache addresses this through Oracle AI Database redo technology:

### How True Cache Stays Synchronised:

**Cache stays synchronised using Oracle AI Database redo technology:**
The same redo stream that drives Data Guard standbys is used to propagate changes from the primary database to True Cache instances in real time.

**Automatic refresh with no manual invalidation:**
Developers never write cache invalidation code. There are no TTL settings to tune, no event-driven purge jobs to build, and no risk of a missed invalidation leaving users with wrong data.

**Consistency maintained across everything related to cached data:**
True Cache maintains transactional consistency. If a transaction updates three related rows, all three updates arrive at True Cache as a single atomic unit.

**Eliminates application-managed caching:**
The application simply issues SQL. Oracle routes reads to True Cache and ensures the data is always current. The caching tier is invisible to application code.

## Scale Out with Multiple True Cache Instances

A single True Cache instance already delivers significant read offload. For even greater throughput and availability, multiple instances can be deployed simultaneously:

### Deployment Options:

**Higher availability:**
Read requests are distributed across instances. The failure of one True Cache instance does not interrupt read availability, other instances continue serving requests.

**Cache larger data sets:**
Aggregate memory across multiple True Cache nodes to hold the entire working set in memory. Each instance can be sized independently based on the data it serves.

**Group isolation:**
Different True Cache instances can be configured to serve different application groups. An HR application can warm its own data set in one instance while a Sales application does the same in another, providing predictable performance and preventing workload interference.

**Overflow to disk:**
Optionally, True Cache can overflow data to local disk when memory is full. This is still significantly faster than accessing the back-end primary database, extending the effective cache size beyond available RAM.

All instances receive the same redo stream from the primary database and remain transactionally consistent regardless of how many are deployed.

## Deploying True Cache Close to the User

For use cases involving data residency requirements, user proximity, or device proximity, applications are often deployed far from the central database. In such cases, True Cache can be deployed near the application to boost read performance significantly.

### Geographic Deployment Benefits:

**Proximity reads:**
True Cache deployed in the same region or data centre as the application eliminates wide-area network latency from the read path entirely. Reads are served locally at memory speed.

**Data residency compliance:**
True Cache does not store any data on disk by default. This means it functions as a pure data-processing tier, one that data residency regulations typically allow to exist in proximity to users, even when the primary database must remain in a specific jurisdiction.

**Transparent cache warming:**
When a True Cache instance near the user does not yet have a requested object in memory (a cache miss), it fetches the data silently from the primary database and warms up completely transparently to the application.

**Writes remain authoritative:**
Write operations always travel to the centralised primary database regardless of where True Cache is deployed, ensuring a single source of truth.

## How Your Business Can Benefit from Oracle True Cache

### Cost Savings:
- **Improve application performance without rewriting applications** - no development cost to adopt True Cache
- **No risk and complexity of additional caching products and skills** - eliminate the operational overhead of a separate caching tier
- **Single cache for different data types and formats** - one service handles document, relational, row, and columnar data
- **Offload caching to commodity hardware from the database** - right-size the primary database and serve reads from lower-cost nodes
- **Stronger security, which comes with Oracle AI Database** - security, auditing, and encryption extend to the cache tier automatically
- **Leverage the full power of Oracle AI Database** - True Cache is a first-class feature, not a bolt-on

## Customer Usage Examples

Oracle True Cache is already running production workloads across industries:

| Industry | Use Case |
|---|---|
| **Stock Exchange** | Read-heavy stock ticker workloads offloaded to True Cache, eliminating database bottlenecks at market open |
| **Financial Institution** | Fraud detection AI inferencing served from True Cache at memory speed, reducing detection latency |
| **Marketing** | Real-time personalised campaigns without stale cached data reaching customers |
| **Oracle Fusion Applications** | Business object layer caching for infrequently changing reference data |
| **Oracle Banking Applications** | Read-intensive core banking workloads offloaded to cache, freeing primary DB capacity |

## Technical Summary

### How True Cache Fits in Your Architecture:

```
Application
    │
    ├── READ  ──────────────►  True Cache (memory, microseconds)
    │                               │
    │                         (redo sync, automatic)
    │                               │
    └── WRITE ──────────────►  Primary Oracle AI Database
```

- **Reads**: Served from True Cache at microsecond latency
- **Writes**: Routed to Primary DB for full ACID durability
- **Sync**: Redo technology propagates changes instantly, no application involvement

### Supported Data Types:
- Relational (row format)
- JSON / Document
- Columnar
- Any data accessible via SQL

### Deployment Flexibility:
- Single instance for basic offload
- Multiple instances for scale-out and group isolation
- Geographically distributed instances for proximity reads
- Overflow to disk for working sets larger than available memory


## Learn More

- [Oracle True Cache Documentation](https://www.oracle.com/database/truecache/)


## Acknowledgements

- **Author**: Francis Regalado, Database Product Manager
- **Contributors**: 
- **Last Updated**: Francis Regalado, February 2026
