# Introduction

## About this Demo

**JSON Relational Duality** in Oracle Database 23ai lets you build apps that **think in JSON** while the database **stores data relationally**—with **zero duplication**, strong consistency, and full SQL power. Duality Views expose **updatable JSON business objects** while Oracle maintains a **normalized schema** behind the scenes. You get one source of truth, multiple access paths (JSON APIs, REST, MongoDB-compatible API, SQL), and **enterprise-grade security**—without ORMs or fragile duplication.

You may add an optional video, using this format: [](youtube:YouTube video id)

[](youtube:REPLACE_WITH_VIDEO_ID)

### Try the Interactive Demo

Launch the HTML demo here:
- <a href="./interactiveJson.html" target="_blank">Open the First interactive demo</a>


What you'll see in 1.0:
- **Introduction**: Why JSON Relational Duality for enterprise apps
- **Core Concept**: Treat data as JSON and relational tables—no trade-offs
- **Dual Views in Action**: Edit JSON → watch simulated normalized tables update
- **ETAG Concurrency**: Lock-free updates via If-Match (optimistic control)
- **Code Examples**: SQL Duality Views, REST with ETAG, MongoDB-compatible snippets
- **Metrics + Workflow Guide**: Live counters and a collapsible, step-by-step tour

What you’ll see 2.0:

* **Introduction**: Why JSON Relational Duality for enterprise apps
* **Core Concept**: Treat data as JSON *and* relational tables—no trade-offs
* **Duality View Explorer**: Paste JSON → see simulated normalized tables and indexes
* **ETAG Concurrency**: Lock-free updates via `If-Match` (optimistic control)
* **Code Examples**: SQL Duality Views, REST with ETAG, MongoDB-compatible snippets
* **Recap**: Benefits, deployment options, and next steps

### Why Use JSON Relational Duality

Duality removes the json-vs-relational either/or decision. Model and ship in JSON while keeping relational strength for analytics, integrity, and operations.

Key benefits:

* **One model, many interfaces**: Work with the same business object via JSON APIs, REST, MongoDB-compatible API, and SQL—no duplication
* **Updatable JSON with relational storage**: Duality Views map JSON to normalized tables in the kernel—**ORMs become unnecessary**
* **Consistency by design**: Avoid copy/paste document sprawl; keep data consistent and analytics-ready
* **SQL analytics on JSON data**: Run joins, aggregates, and BI over the same objects without ETL
* **Lock-free concurrency**: **ETAG** support for safe, optimistic updates across APIs
* **Enterprise-grade**: Fine-grained, field-level controls; governance, auditing, backup/recovery, and manageability you expect from Oracle Database
* **Works everywhere**: On-prem (Exadata/ODA), OCI (Autonomous DB, Exadata DB Service, Base DB Service), and multicloud (Oracle Database @ Azure/Google Cloud/AWS), plus Always Free and downloadable images
* **Lower complexity & cost**: Unified data platform reduces middleware, duplication, and latency

## Learn More
- Product Page: https://www.oracle.com/database/what-is-json/technologies/database/

- Related Livelabs Workshop : https://livelabs.oracle.com/pls/apex/r/dbpm/livelabs/view-workshop?wid=3635

- Oracle JSON Developer's Guide (Docs) : https://docs.oracle.com/en/database/oracle/oracle-database/23/adjsn/overview-json-oracle-database.html

## Acknowledgements
- Author — Francis Regalado
- Contributors — David Start, William Masdon
- Last Updated By/Date — Francis Regalado, September 2025
