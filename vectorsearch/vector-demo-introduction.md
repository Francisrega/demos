# Introduction

## About this Demo

Oracle AI Vector Search brings semantic search to Oracle Database 23ai by storing and indexing embeddings directly in the database. This interactive demo showcases how vector embeddings represent meaning, how similarity search retrieves semantically related items, and how these capabilities enable real-world applications like intelligent document search, recommendations, and image similarity.


You may add an optional video, using this format: [](youtube:YouTube video id)

[](youtube:REPLACE_WITH_VIDEO_ID)


### Try the Interactive Demo

Launch the HTML demo here:
- <a href="./vector-demo.html" target="_blank">Open the Interactive Demo</a>


What you’ll see:
- Introduction: High-level overview of vector search
- Embeddings: Generate and visualize example embeddings
- Search: Try a semantic similarity search workflow
- Use Cases: Explore example applications and mini-demos
- Code: See example SQL, HNSW indexing, and client code

### Why Use AI Vector Search

Vector search understands meaning, not just keywords. By representing content as high-dimensional vectors, you can retrieve results that are contextually relevant—even when exact words don’t match.

Key benefits:
- Semantic relevance beyond keywords: Find similar items by meaning
- Unified data platform: Combine vectors with relational, JSON, and graph data in Oracle Database 23ai
- Performance at scale: HNSW indexing and efficient distance metrics (cosine, Euclidean, dot product)
- Enterprise-grade: Security, backup/recovery, and manageability you expect from Oracle Database
- Modern AI patterns: Power Retrieval Augmented Generation (RAG), recommendations, deduplication, and clustering
- Multimodal readiness: Apply vector search to text, images, and more
- Simpler architecture: Keep data and AI search in the same platform to reduce complexity and latency



- Vector Search Guide (Docs): https://docs.oracle.com/en/database/oracle/oracle-database/23/vecse/
- Product Page: https://www.oracle.com/database/ai-vector-search/
- Related LiveLabs Workshop: https://livelabs.oracle.com/pls/apex/f?p=133:180:114898719666832::::wid:4166

## Acknowledgements
- Author — William Masdon 
- Contributors — Francis Regalado, Brianna Ambler, Ley Sylvester, Mary Hess
- Last Updated By/Date — Francis Regalado, October 2025


# Introduction

## About Oracle AI Vector Search

Oracle AI Vector Search is a breakthrough capability in Oracle Database 23ai that enables searching data by semantic meaning rather than just keywords. This technology bridges the gap between traditional structured data and the growing volume of unstructured business data - documents, images, support tickets, and more - allowing you to search them all by their conceptual content.

This interactive demonstration uses a real-world support incident system to show how vector embeddings transform database search from simple pattern matching to intelligent semantic understanding.

[](youtube:REPLACE_WITH_VIDEO_ID)


The interactive demo requires no setup or prerequisites. Simply click through the workflow to:
- Observe the transformation from text to vectors
- Compare traditional versus semantic search results
- Watch real-time clustering visualization
- See actual similarity percentages
- Understand how different types of issues naturally organize

Each step displays the underlying SQL operations, making it easy to understand and apply these concepts to your own use cases.

### **Try the Interactive Demo**
Note: You can minimze the menu by clicking '≡' to better interactive with the demo.


<iframe src="../vector-demo.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>


### What You'll Discover

**Through the Interactive Demo:**
- How support incidents with different descriptions but similar meanings automatically cluster together
- Why "system crash," "spontaneous reboot," and "freeze" are found together despite sharing no common keywords
- The dramatic difference between traditional LIKE searches and semantic similarity search
- How similarity scoring works on a 0-100% scale
- Real-time visualization of how vectors organize themselves in semantic space

**Key Concepts You'll Understand:**
- **Vectors as Semantic Fingerprints**: Mathematical representations that capture meaning
- **The Similarity Property**: Similar content produces vectors that are mathematically close together
- **Distance Metrics**: How databases measure conceptual similarity using cosine, Euclidean, and other formulas
- **Converged Database Advantage**: Unifying vector search with relational, JSON, and graph capabilities

**The Power of Similarity:**
When a support ticket describes "system became unresponsive," the database understands this is semantically similar to "computer crashed" - even though they share no common words. This happens because their vector representations are mathematically close in high-dimensional space.

The demo visualizes this by showing:
- Crash-related issues clustering together
- Performance problems forming their own group
- Hardware issues creating another cluster
- Unrelated problems (like printer jams) appearing far from computer issues


**The Problem with Traditional Search:**
A keyword search for "crash" completely misses:
- "System became unresponsive"
- "Computer froze during operation"
- "Application stopped working"
- "Blue screen appeared"
- "Unexpected restart occurred"

**The Vector Search Solution:**
All these descriptions are automatically recognized as semantically related. They appear close together in vector space and are returned together in search results, regardless of the specific words used.

### Flexible Vector Generation

Oracle provides four approaches for creating embeddings:
1. **Pre-created vectors** from external systems
2. **Database-integrated embedding** using DBMS_VECTOR functions
3. **Application-layer generation** with your preferred libraries
4. **In-database models** using ONNX for complete data locality

The demo showcases approach #2, demonstrating how text is converted to vectors using built-in database functions.


## Learn More

- [AI Vector Search Documentation](https://docs.oracle.com/en/database/oracle/oracle-database/23/vecse/overview-ai-vector-search.html)
- [LiveLabs Hands-On Workshops](https://livelabs.oracle.com/pls/apex/f?p=133:180:114898719666832::::wid:4166)
- [Always Free Autonomous Database](https://www.oracle.com/autonomous-database/free-trial/)
- [Oracle Database 23ai Free](https://www.oracle.com/database/free/get-started/)

## Acknowledgements
- Author — Francis Regalado
- Contributors — William Masdon, Brianna Ambler, Ley Sylvester, Mary Hess, David Start
- Last Updated By/Date — Francis Regalado, October 2025
