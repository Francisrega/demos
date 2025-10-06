# Introduction
About Oracle AI Vector Search

Oracle AI Vector Search is a breakthrough capability in Oracle Database 23ai that enables searching data by semantic meaning rather than just keywords. This technology bridges the gap between traditional structured data and the growing volume of unstructured business data - documents, images, support tickets, and more - allowing you to search them all by their conceptual content.

This interactive demonstration uses a real-world support incident system to show how vector embeddings transform database search from simple pattern matching to intelligent semantic understanding.

The interactive demo requires no setup or prerequisites. Simply click through the workflow to:

Observe the transformation from text to vectors

Compare traditional versus semantic search results

Watch real-time clustering visualization

See actual similarity percentages

Understand how different types of issues naturally organize

Each step displays the underlying SQL operations, making it easy to understand and apply these concepts to your own use cases.

Try the Interactive Demo

Note: You can minimze the menu by clicking '≡' to better interactive with the demo.

<iframe src="../vector-demo.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>
What You'll Discover

Through the Interactive Demo:

How support incidents with different descriptions but similar meanings automatically cluster together

Why "system crash," "spontaneous reboot," and "freeze" are found together despite sharing no common keywords

The dramatic difference between traditional LIKE searches and semantic similarity search

How similarity scoring works on a 0-100% scale

Real-time visualization of how vectors organize themselves in semantic space

Key Concepts You'll Understand:

Vectors as Semantic Fingerprints: Mathematical representations that capture meaning

The Similarity Property: Similar content produces vectors that are mathematically close together

Distance Metrics: How databases measure conceptual similarity using cosine, Euclidean, and other formulas

Converged Database Advantage: Unifying vector search with relational, JSON, and graph capabilities 

AI Vector Search - one pager

The Power of Similarity:
When a support ticket describes "system became unresponsive," the database understands this is semantically similar to "computer crashed" - even though they share no common words. This happens because their vector representations are mathematically close in high-dimensional space.

The demo visualizes this by showing:

Crash-related issues clustering together

Performance problems forming their own group

Hardware issues creating another cluster

Unrelated problems (like printer jams) appearing far from computer issues

The Problem with Traditional Search:
A keyword search for "crash" completely misses:

"System became unresponsive"

"Computer froze during operation"

"Application stopped working"

"Blue screen appeared"

"Unexpected restart occurred"

The Vector Search Solution:
All these descriptions are automatically recognized as semantically related. They appear close together in vector space and are returned together in search results, regardless of the specific words used.

Business Value (for your stakeholders)

Lower TCO & complexity — Do similarity search in the database alongside business data; avoid moving data to a separate vector store and the integration/security overhead that comes with it. 

AI Vector Search - one pager

Enterprise-grade by default — Because AI runs inside Oracle Database, you inherit HA, performance, and security: Partitioning, RAC, Sharding, Exadata, Data Guard, TDE, Key Vault, Audit Vault, VPD, and more. 

AI Vector Search - one pager

Deploy anywhere you already run Oracle — Cloud, on-prem, hybrid; VMs, containers, Kubernetes. A feature of Oracle Database 23ai. 

AI Vector Search - one pager

Ready now — Load an embedding model via ONNX, generate vectors, and query with vector_distance() alongside SQL filters. 

AI Vector Search - one pager

RAG-ready — Retrieve governed business context for LLMs to reduce hallucinations without retraining on sensitive data. 

AI Vector Search - one pager

Included — AI Vector Search is a no-charge feature in every Oracle Database 23ai edition. 

AI Vector Search - one pager

Role-Based Talking Points

CIO / VP Apps: Less to buy and run; faster time-to-value using existing Oracle investments. 

AI Vector Search - one pager

Enterprise Architect: Converged architecture—compose vector + relational + JSON in one system; fewer moving parts. 

AI Vector Search - one pager

Data/AI Team: Use ONNX embeddings; combine similarity and business filters in SQL; ops stays simple. 

AI Vector Search - one pager

Support Ops: Find “tickets like this” by meaning (crash/reboot/freeze) instead of brittle keywords.

KPIs to Track in Pilots

Search success rate and first-touch resolution

MTTR (mean time to resolution) and escalation/deflection rate

Ops simplification: systems and nightly sync jobs eliminated

Cost deltas from removing a separate vector tier

Flexible Vector Generation

Oracle provides four approaches for creating embeddings:

Pre-created vectors from external systems

Database-integrated embedding using DBMS_VECTOR functions

Application-layer generation with your preferred libraries

In-database models using ONNX for complete data locality 

AI Vector Search - one pager

The demo showcases approach #2, demonstrating how text is converted to vectors using built-in database functions.