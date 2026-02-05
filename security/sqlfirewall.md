# Introduction

## About Oracle SQL Firewall

**Oracle SQL Firewall** is a kernel-resident security control built directly into Oracle AI Database 26ai that provides real-time protection against SQL injection attacks. Unlike application-based firewalls or Web Application Firewalls (WAFs) that rely on pattern matching, SQL Firewall operates at the database kernel level, the last line of defense before malicious SQL executes.

SQL Firewall learns normal SQL traffic patterns, creates an allow-list of legitimate SQL statements and connection contexts, and then enforces that policy by blocking any SQL that doesn't match. This allow-list approach protects against both known and unknown attack patterns, including zero-day exploits that bypass traditional defenses.

SQL injection remains one of the most critical database security threats, consistently ranking #3 in the OWASP Top 10 for web application vulnerabilities. With 42% of attacks on public-facing systems being SQL injection-based, organizations need protection that works even when application-level defenses fail.

[Video hosted on Oracle Video Hub](videohub:)

### **Try the Interactive Demo**
Note: You can minimize the menu by clicking '≡' to better interact with the demo.

<iframe src="../sqlfirewall.html" width="100%" height="1100px" frameborder="0" style="min-width: 100%; min-height: 1100px; height: 1100px !important;" ></iframe>

###  
### 

### What You'll Discover:

- **The SQL Injection Threat**: See how attackers exploit vulnerable applications by injecting malicious SQL that bypasses authentication and accesses unauthorized data.
- **Traditional Defenses Fall Short**: Understand why application-level fixes and Web Application Firewalls often fail to prevent sophisticated SQL injection attacks.
- **Three-Step Protection**: Watch SQL Firewall enable protection, learn normal SQL patterns, and enforce policies to block attacks in real-time.
- **Kernel-Resident Architecture**: Discover how being built into the database kernel allows SQL Firewall to see ALL traffic, network connections, stored procedures, internal jobs, and more.
- **Real Attack Blocking**: Experience how SQL Firewall detects unauthorized SQL signatures, logs violations, and blocks attacks before they reach the database execution engine.
- **Continuous Animation**: See SQL packets flow through the system, the shield activate when protection is enforced, and attacks blocked with particle effects.

### Key Benefits:

- **Last Line of Defense**: SQL Firewall protects at the database kernel level, stopping SQL injection attacks that bypass application controls and WAFs.
- **Allow-List Approach**: Unlike pattern-based systems, SQL Firewall learns legitimate SQL and blocks everything else, protecting against zero-day exploits.
- **Kernel-Resident Architecture**: Built into the database engine, SQL Firewall sees ALL SQL traffic including bequeath connections, stored procedures, and internal jobs that network firewalls miss.
- **Minimal Performance Impact**: Less than 1-1.5% CPU overhead with no observable latency, making it practical for production deployments.
- **No Client Changes Required**: Simple, scalable deployment across your database fleet with no client-side configuration or networking changes.
- **Comprehensive Visibility**: Logs all violations with full context (SQL text, IP address, OS user, program name) for security monitoring and forensics.
- **Dual Protection Modes**: Can operate in observe-only mode for monitoring or blocking mode for active protection.
- **Works Everywhere**: Available in Oracle AI Database 26ai across on-prem, OCI, multicloud, Always Free tier, and downloadable database images.

### The Challenge SQL Firewall Solves:

SQL injection attacks continue to plague data-driven applications despite decades of awareness:

**Application Defenses Are Unreliable**: Developers make mistakes, code reviews miss problems, and new vulnerabilities are discovered constantly. Traditional approaches like input validation, prepared statements, and avoiding dynamic queries often fail in practice. Even with the best development practices, a single overlooked input field can expose the entire database.

**WAFs Have Limited Effectiveness**: Web Application Firewalls use regular expression patterns to detect known SQL injection payloads, but they're helpless against zero-day exploits. They can't evaluate the actual content of injection payloads and can't use full SQL context when making decisions. Attackers continuously evolve their techniques to bypass pattern-based detection.

**Network Firewalls Have Blind Spots**: External database firewalls can only monitor SQL traffic over the network, missing stored procedure execution, bequeath connections, and local connections. They require complex in-line deployment, create single points of failure, and struggle with encrypted traffic. They also can't see the real object information like CURRENT_SCHEMA or resolve synonyms.

**The Last Line of Defense**: SQL Firewall operates at the database kernel level, the last possible interception point before malicious SQL executes. It understands SQL intent through parsing rather than pattern matching, and enforces allow-lists that protect against both known and unknown attack patterns.

### How It Works:

SQL Firewall follows a simple three-step process that makes protection straightforward:

**1. Enable**: Activate SQL Firewall for your target database with a single command. The firewall becomes active in the database kernel with minimal overhead. Grant SQL_FIREWALL_ADMIN privileges to a security administrator and enable the feature globally with `DBMS_SQL_FIREWALL.ENABLE`.

**2. Capture & Learn**: Allow SQL Firewall to observe normal application SQL traffic during a learning period (typically 24-48 hours). It captures SQL signatures - normalized statements with bind variables - and execution contexts including client IP addresses, OS usernames, and program names. This builds a comprehensive allow-list of legitimate database activity.

**3. Enforce**: Deploy the allow-list policy and enforce it with `ENABLE_ALLOW_LIST`. SQL Firewall checks every incoming SQL statement against the allow-list, logging violations and optionally blocking unauthorized SQL before it executes. Any mismatch triggers a violation that is logged to `DBA_SQL_FIREWALL_VIOLATIONS` and returns ORA-47605 error to the application.

### Advanced Capabilities:

**Execution Context Enforcement**: Beyond just SQL signatures, SQL Firewall can enforce trusted connection paths by verifying client IP addresses, OS usernames, and program names - protecting against compromised credentials. If legitimate credentials are used from unexpected locations or programs, SQL Firewall detects and blocks the attempt.

**Flexible Management Options**: Administer SQL Firewall through multiple interfaces:
- Oracle Data Safe (centralized OCI console management)
- DBMS_SQL_FIREWALL PL/SQL package (direct database administration)
- Oracle Enterprise Manager (enterprise-wide monitoring and control)

**Integration with Database Vault**: SQL Firewall is included with Oracle Database Vault, allowing you to combine realm protection (schema and object protection), command rules (operation control), and SQL statement allow-lists (SQL Firewall) for holistic database security. This defense-in-depth approach provides multiple layers of protection.

**Comprehensive Audit Trail**: All violations are logged to `DBA_SQL_FIREWALL_VIOLATIONS` with full context:
- Exact SQL text that was attempted
- Username and session information
- Client IP address and program name
- OS username
- Timestamp and violation cause
- Whether the statement was blocked

This enables security monitoring, forensic analysis, compliance reporting, and detection of attack patterns.

**Gradual Deployment**: Start with observe-only mode (`enforce => DBMS_SQL_FIREWALL.OBSERVE`) to understand your SQL patterns without impacting applications. Monitor the violations log to identify legitimate SQL that wasn't captured during the learning period. Once confident in the allow-list coverage, transition to blocking mode (`block => TRUE`) for active protection.

### Real-World Protection Scenarios:

**Mitigate SQL Injection Risks**: Block attacks that bypass application input validation, protecting against unauthorized data access, data modification, privilege escalation, and data exfiltration. Common attack patterns like `' OR '1'='1` or union-based injection are stopped before execution.

**Detect Compromised Credentials**: Identify when legitimate database credentials are used from unexpected locations, programs, or IP addresses, catching credential theft and insider threats. For example, if an application service account suddenly connects from an administrator's workstation instead of the application server.

**Prevent Application Bypass**: Stop users from bypassing application logic by connecting directly to the database with tools like SQL*Plus, SQL Developer, or third-party query tools. Only connections from approved programs are allowed.

**Protect Legacy Applications**: Add a security layer to applications that can't be easily modified, protecting vulnerable code without application changes. This is especially valuable for purchased applications where source code isn't available or for legacy systems where modification carries high risk.

**Enforce Least Privilege**: Ensure database users can only execute the specific SQL statements they need for their role. Even if an account is compromised, the attacker is limited to the allow-listed SQL operations.

### SQL Firewall vs. Network Database Firewall:

Both Oracle SQL Firewall (kernel-resident) and Oracle Audit Vault and Database Firewall (AVDF, network-based) provide SQL injection protection, but they have different strengths:

**SQL Firewall Advantages**:
- Simple, scalable deployment with no networking changes
- Sees ALL traffic including local connections and stored procedures
- Minimal CPU overhead (1-1.5%) with no latency
- No single point of failure
- Works with encrypted connections without TLS termination
- Can see real object information (schemas, synonyms)

**Database Firewall (AVDF) Advantages**:
- Supports non-Oracle databases (MySQL, MS-SQL, IBM DB2, SAP Sybase)
- Protects Oracle Database versions 21c and below
- Zero performance overhead on database server (in monitoring mode)
- Can be deployed without database changes

**When to Use Each**:
- Use SQL Firewall for Oracle Database 23ai and later when you want kernel-level protection with zero networking complexity
- Use AVDF when protecting non-Oracle databases or Oracle versions before 23ai
- Use both together for defense-in-depth, SQL Firewall provides kernel protection while AVDF monitors network traffic and provides a centralized view across your database fleet

For comprehensive protection, both can be used together. SQL Firewall is included free with the AVDF license for Oracle databases.

### Performance and Scalability:

**Minimal Overhead**: SQL Firewall adds less than 1-1.5% CPU overhead in production environments. This minimal impact comes from efficient kernel-level implementation that avoids expensive operations like network proxying or external process calls.

**No Observable Latency**: Query response times are not affected because SQL Firewall's signature checking is highly optimized and happens in-memory within the database kernel. The allow-list is indexed for fast lookup.

**Scales with Database**: Because SQL Firewall is built into the database kernel, it automatically scales with your database infrastructure. In Oracle RAC environments, the allow-list is shared across all instances. With Exadata, you get both SQL Firewall protection and Exadata's performance advantages.

**Production-Ready**: Organizations run SQL Firewall in production environments protecting mission-critical databases processing thousands of transactions per second with no performance degradation.

## Learn More

- [Oracle SQL Firewall Documentation](https://docs.oracle.com/en/database/oracle/oracle-database/23/dbseg/using-oracle-sql-firewall.html)
- [Oracle Data Safe SQL Firewall](https://docs.oracle.com/en-us/iaas/data-safe/doc/sql-firewall.html)
- [LiveLabs SQL Firewall Workshop](https://livelabs.oracle.com/pls/apex/f?p=133:100:::::SEARCH:sql%20firewall)
- [SQL Injection Mitigation Technical Report](https://www.oracle.com/a/ocom/docs/database/oracle-database-sql-firewall.pdf)
- [Always Free Autonomous Database](https://www.oracle.com/autonomous-database/free-trial/)
- [Oracle AI Database Free](https://www.oracle.com/database/free/get-started/)

## Acknowledgements

- Author - Francis Regalado, Database Product Manager
- Contributors - 
- Last Updated By/Date - Francis Regalado, February 2026
