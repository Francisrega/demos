# Introduction

## About this Demo

Enterprises want AI agents — but building them is hard. Traditional AI adoption requires stitching together secure data access, model hosting, CI/CD, monitoring, and evaluation across multiple tools and frameworks with steep learning curves. Worse, private enterprise data cannot be sent to public LLMs — AI must be brought to the data, not the other way around. The result: production-grade AI is slow, fragile, and expensive to build at scale.

**The Challenge**: Organizations face three converging pressures. AI adoption complexity makes it difficult to assemble production-grade pipelines. Enterprise data constraints prevent sensitive data from being shared with public LLMs due to compliance, governance, and security requirements. And a rapidly changing, fragmented agent ecosystem means open-source tools often miss licensing, enterprise support, and standardization.

**What if you could build AI agents in minutes — with no code — entirely inside your enterprise security boundary?**

## The Solution: Oracle AI Database Private Agent Factory

**Oracle AI Database Private Agent Factory (PAF)** is a no-code platform to rapidly build, evaluate, deploy, and operate intelligent AI agents securely and at scale. It runs inside or alongside the Oracle AI Database, bringing AI directly to business-critical data and eliminating data movement to public LLMs.

### End-to-End Agent Lifecycle:
- Visual Agent Builder and runtime orchestration
- Pre-built agents for knowledge, data analysis, and deep research
- Secure model serving via Oracle Private AI Services Container
- Grounding, guardrails, monitoring, and extensibility

### Built Where Enterprise Data Lives:
- Runs inside or alongside the Oracle AI Database
- Brings AI directly to business-critical data
- Eliminates data movement to public LLMs, ensuring security and compliance

### **Try the Interactive Demo**
Note: You can minimize the menu by clicking '≡' to better interact with the demo.

<iframe src="paf.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>

###  
### 

### What You'll Discover:

- **Build Agent**: Watch the visual Agent Builder canvas come to life — toolbar nodes activate one by one, then five workflow nodes (Trigger, LLM, DB Lookup, Tool Call, Output) snap into place with animated connector lines showing execution flow. No code written.

- **Knowledge RAG**: See how enterprise sources (SharePoint, websites, PDFs, Oracle AI Database tables) are ingested and vectorized privately using Oracle AI Vector Search. A real user query is answered with a fully sourced, traceable response — 100% inside the Oracle security boundary.

- **Analyze Data**: Experience the Data Analysis Agent connecting to Oracle AI Database and translating a natural language prompt into SQL, then auto-generating a regional revenue breakdown chart with an AI-written narrative insight. Zero SQL knowledge required.

- **Govern & Guard**: Observe the governance perimeter assembling: SSO and role-based access controls, the Private AI Container locking down LLM and embedding inference, a central zero-leakage boundary shield, guardrails for safety filtering, and full compliance audit logging.

- **Deploy Anywhere**: Follow the complete architecture from business user through Agent Builder and PAF Runtime to Oracle AI Database and Private LLM — deployable on-prem, OCI, or any cloud using a portable Agent Spec.

## What You Get at a Glance

**Simplicity — No-code for all:**
- Business users and developers build, test, and deploy agents
- Drag-and-drop Agent Builder with reusable templates
- No coding or custom orchestration required
- Pre-built agents and agent templates ready from day one

**Privacy and Security — Access and authorization controls:**
- Private AI Services Container for embeddings and LLM inference
- SSO, access and authorization, sharing controls
- All AI inference runs inside the enterprise perimeter

**Performance and Portability — Deploy anywhere:**
- Deploy on-prem, or on any cloud IaaS privately
- Broad model choice, export/import via Agent Spec
- Multi-modal Vector AI Search-powered RAG agents
- Choice of LLMs enhances portability across environments

**Governance and Safety:**
- Guardrails and evaluation workflows built in
- Evaluation of models for safety before deployment
- Audit trails and compliance policy enforcement

## Agents in Action

### Knowledge-Based AI Agent (RAG)

The Knowledge-Based AI Agent securely ingests enterprise content from SharePoint, websites, and file systems, grounding responses with Oracle AI Vector Search for accurate, traceable, and source-linked answers.

**How it works:**
1. Enterprise sources are connected — SharePoint, internal websites, HR and compliance PDFs, and Oracle AI Database tables
2. Documents are chunked and vectorized using Oracle AI Vector Search, entirely within the enterprise perimeter
3. A user submits a natural language question
4. Semantic similarity search retrieves the most relevant source chunks
5. The LLM generates a response grounded in retrieved content, with source citations

**Key capabilities:**
- Accurate, traceable answers with source links
- No data ever sent to a public LLM
- Supports SharePoint, file systems, websites, and databases
- Powered by Oracle AI Vector Search

### Data Analysis Agent

The Data Analysis Agent connects natively to Oracle AI Database, understands tables and views, generates insights, explains complex data, and automatically creates visualizations for faster decision-making.

**How it works:**
1. The agent auto-discovers available tables and views in Oracle AI Database
2. A business user asks a question in plain language
3. The agent generates and executes SQL internally
4. Results are returned as a narrative insight with auto-generated visualization
5. No SQL knowledge required from the end user

**Key capabilities:**
- Natural language to SQL, entirely inside Oracle
- Auto-generated charts and visualizations
- Explains complex data in plain business language
- Built-in Oracle Database best practices

## Agent Builder

The Visual Agent Builder lets users create agents using a drag-and-drop canvas — no code required. Business users and engineers can prototype and deploy agents in minutes.

### Builder Components:
- **Trigger Node** — Entry point for user queries or scheduled events
- **LLM Node** — Reasoning and language generation with your choice of model
- **DB Lookup Node** — Secure connection to Oracle AI Database tables and views
- **Tool Call Node** — SQL execution, REST API calls, or custom functions
- **Output Node** — Response formatting and delivery

### Agent Spec:
Every agent designed in the builder is exported as a portable `agent-spec.yaml` file — enabling version control, team collaboration, and deployment across environments without rebuilding.

### Run, Orchestrate, and Scale:
Agents execute in a managed Agent Runtime with full orchestration. Choose the model you want. Scale from prototype to production with no rearchitecting.

## Enterprise Governance & Safety

### Zero Data Leakage Architecture
Oracle AI Database Private Agent Factory is built on a fundamental principle: **AI is brought to the data — not data to the AI.** All LLM inference, embedding generation, and retrieval runs inside the Oracle perimeter.

### Security Controls:
- **SSO and Authorization** — Role-based access control applied to all agent interactions and data sources
- **Private AI Services Container** — Embeddings and LLM inference run inside enterprise boundaries, never reaching public endpoints
- **Sharing Controls** — Fine-grained control over who can view, run, or modify agents and models

### Safety and Compliance:
- **Guardrails** — Safety filters and topic restrictions applied before and after LLM inference
- **Evaluation Workflows** — Systematic model evaluation for safety, accuracy, and bias before deployment
- **Audit Trails** — Every agent call logged for governance, auditability, and compliance reporting
- **SOX / GDPR / HIPAA-ready** — Governance framework supports major regulatory requirements

## Portability and Deployment

### Deploy Anywhere
Oracle AI Database Private Agent Factory is designed for maximum portability. The same agent built in the visual designer can be deployed across environments using the Agent Spec format.

### Supported Deployment Targets:
- Oracle Cloud Infrastructure (OCI)
- On-premises Oracle Database environments
- Any cloud IaaS (AWS, Azure, GCP) with Oracle Database
- Hybrid environments combining on-prem and cloud

### Model Choice:
- Connect to Oracle-hosted private LLMs via the Private AI Services Container
- Integrate third-party models with broad LLM compatibility
- Switch models without rebuilding agents — the Agent Spec abstracts the model layer

### Export and Import:
Agents are fully portable via the Agent Spec format, enabling teams to share, version-control, and migrate agents across environments without vendor lock-in.

## Business Outcomes

Organizations deploying Oracle AI Database Private Agent Factory achieve:

- **Sensitive data remains inside the Oracle environment** — compliance and security requirements are met from day one
- **Faster access to trusted knowledge and insights** — employees get accurate, source-linked answers without manual research
- **Reduced operational complexity** — no custom agent development, no framework stitching, no infrastructure assembly
- **Production-ready AI with built-in governance** — guardrails, audit trails, and evaluation workflows built in, not bolted on
- **Broad LLM choice with full portability** — avoid vendor lock-in while maintaining enterprise-grade security

## Business Challenge & Solution

### Challenge:
Enterprise data is spread across databases, documents, and file systems. Employees struggle to quickly find trusted information and insights. Building AI agents that respect compliance and governance requirements has historically required months of custom engineering.

### Solution:
Deploy Oracle AI Database Private Agent Factory to bring AI directly to enterprise data. Use prebuilt agents to accelerate deployment with no custom development. The platform handles orchestration, security, grounding, and governance — so teams can focus on the business problem, not the infrastructure.

### Agents in Action:

**Knowledge-Based AI Agent**
Provides accurate, traceable, source-linked answers using Oracle AI Vector Search — grounded in SharePoint, websites, file systems, and Oracle Database content.

**Data Analysis Agent**
Generates insights, explains complex data, and creates visualizations from Oracle AI Database — using natural language, no SQL required.

## Learn More

- Oracle AI Database Documentation: https://docs.oracle.com/en/database/oracle/oracle-database/

- Oracle Private Agent Factory Documentation: https://docs.oracle.com/en/database/oracle/agent-factory/25.3/paias/


## Acknowledgements

- **Author**: Francis Regalado, Database Product Manager
- **Contributors**: 
- **Last Updated**: Francis Regalado, February 2026
