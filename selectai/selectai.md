# Introduction

## About this Demo

**Oracle Select AI** enables generative AI directly from Oracle Autonomous AI Database and Oracle AI Database. Not only can you ask questions in natural language and get answers from your data without writing SQL, but you can also chat directly with your LLM, generate, synthetic data, translate and summarize text, and build and run AI agents. Select AI turns your database into an AI powered “answer engine” for both structured (tables) and unstructured (documents) content, and more.

Instead of coding your own AI functionality, or leaning multiple APIs and vector databases, Select AI runs inside your database, fully integrated with a wide range of AI providers. It uses your data, whether existing schemas or trusted documents - security, and governance to generate SQL, run Retrieval Augmented Generation (RAG), and even orchestrate multi step AI agents. Business users ask questions in plain English (or other languages depending on LLM capabilities), and Select AI takes care of the prompts, model interactions, SQL, and vector search behind the scenes.

Because Select AI is integrated into Oracle’s converged database, you reduce the distance between users and data: fewer tickets, fewer custom reports, and much faster time from question to insight all while keeping sensitive data where it already lives today.

[Video hosted on Oracle Video Hub](videohub:)


### **Try the Interactive Demo**
Note: You can minimize the menu by clicking '≡' to better interactive with the demo.

<iframe src="../select-ai.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>

###  
### 

### What You’ll Discover:

- **Ask About Sales Data (NL2SQL)**: See how Select AI converts a plain English requests like “Show me our top 5 customers by revenue this year” into an optimized SQL query, runs it, and returns a results table, no SQL knowledge required.
- **Search Company Docs (RAG)**: Explore Retrieval Augmented Generation, where Select AI uses AI Vector Search to find relevant content in your private documents and then provides this content to your LLM to generate a contextually relevant response - reducing hallucinations and keeping answers grounded in your own policies and manuals.
- **Generate Content (AI Chat)**: Use Select AI to draft business-ready content (for example, a customer email about new pricing) via `DBMS_CLOUD_AI.GENERATE`, while still benefiting from database security, audit, and governance.
- **Automate Analysis (Agent)**: Watch an AI Agent orchestrate multi step workflows like analyzing churn risk, identifying at risk customers, and generating a retention campaign by chaining tasks and SQL calls declared from within the database.

### Key Benefits:

- **Natural language to SQL and beyond**: Business users ask questions in everyday language and Select AI generates the SQL, executes it, explains it, and can even narrate results back in plain English.
- **One in-database gateway to many LLMs**: Work with  AI models from OCI Generative AI, OpenAI, Azure OpenAI, Cohere, Anthropic, Bedrock, and more via AI profiles, without rewriting your application logic. Easily switch between providers and models. 
- **Built in RAG with AI Vector Search**: Create vector indexes over your documents declaratively and let Select AI handle embeddings, similarity search, and prompt augmentation for you.
- **Secure, governed, and observable**: Keep data, security policies, and auditing in the database. Select AI uses existing roles, controls, and logging so your AI access is enterprise ready by design.
- **Developer and data scientist friendly**: Use SQL, PL/SQL, and Python APIs to integrate AI into apps, analytics, and pipelines, no separate vector DB or AI control plane to run.
- **Lower TCO, faster insight**: Fewer moving parts, less glue code, and no cross system ETL for AI use cases means lower cost and faster time to value.


## Learn More
- **Select AI SQL generation & usage**: Use Select AI for Natural Language Interaction with your Database :
  https://docs.oracle.com/en-us/iaas/autonomous-database-serverless/doc/select-ai.html


- **6 Simple Tips for Better Text to SQL Generation using Oracle Autonomous Database Select AI**:  
  https://blogs.oracle.com/machinelearning/post/6-simple-tips-for-better-texttosql-generation-using-oracle-autonomous-database-select-ai

- **Select AI Agent** : Build interactive and autonomous agents inside Autonomous AI Database, combining planning, tool use, reflection, and memory to deliver multi-turn workflows.: </br>
  https://docs.oracle.com/en-us/iaas/autonomous-database-serverless/doc/select-ai-agent.html

## Acknowledgements
- Author - Francis Regalado Database Product Manager
- Contributors - David Start, Ley Sylvester 
- Last Updated By/Date - Francis Regalado, December 2025