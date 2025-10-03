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

### Try the Interactive Demo

<iframe src="../vector-demo.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>


## What You'll Discover

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
- Contributors — William Masdon, Brianna Ambler, Ley Sylvester
- Last Updated By/Date — Francis Regalado, October 2025
