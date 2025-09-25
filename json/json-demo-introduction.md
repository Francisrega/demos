# Introduction

## About this Demo

**JSON Relational Duality** in Oracle Database 23ai lets you build apps that **think in JSON** while the database **stores data relationally**—with **zero duplication**, strong consistency, and full SQL power. Duality Views expose **updatable JSON business objects** while Oracle maintains a **normalized schema** behind the scenes. You get one source of truth, multiple access paths (JSON APIs, REST, MongoDB-compatible API, SQL), and **enterprise-grade security**—without ORMs or fragile duplication.

You may add an optional video, using this format: [](youtube:YouTube video id)

[](youtube:REPLACE_WITH_VIDEO_ID)

### Try the Interactive Demo

Launch the HTML demo here:

* <a href="./oracle-json-duality-demo-v7.html" target="_blank">Open the Interactive Demo</a>

What you’ll see:

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

* LiveLab: Build with JSON Duality — [https://apexapps.oracle.com/pls/apex/f?p=133:180:16090110673701::::wid:3635](https://apexapps.oracle.com/pls/apex/f?p=133:180:16090110673701::::wid:3635)
* Oracle Database 23ai Product Page — [https://www.oracle.com/database/](https://www.oracle.com/database/)
* Oracle JSON & Duality Views (Docs) — [https://docs.oracle.com/en/database/oracle/oracle-database/23/](https://docs.oracle.com/en/database/oracle/oracle-database/23/)

> Tip: Host the HTML file from this workshop (e.g., `oracle-json-duality-demo-v7.html`) alongside this page so the **Open the Interactive Demo** link works out of the box.
