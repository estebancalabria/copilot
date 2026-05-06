# Microsoft Purview & Microsoft 365 Data Governance – Complete Study Notes

## 🧠 1. Overview: Why Data Governance Matters

Modern organizations generate massive volumes of data across Microsoft 365 services (Email, Teams, SharePoint, OneDrive, Copilot, logs, and external apps).

This introduces key challenges:

- Data leaks and oversharing
- Regulatory compliance (GDPR, HIPAA, ISO 27001)
- Insider threats (intentional or accidental)
- AI-driven data exposure (Copilot and external AI tools)
- Lack of visibility across distributed systems

👉 Microsoft Purview is Microsoft’s unified platform for:
- Data Governance
- Information Protection
- Compliance & Risk Management

---

## 🏗️ 2. Core Architecture of Microsoft Purview

Purview is organized into three main pillars:

### 🔐 Data Security
Protect sensitive information through classification, labeling, and access control.

### 📊 Data Governance
Ensure data is discoverable, structured, and managed across its lifecycle.

### ⚖️ Risk & Compliance
Detect, investigate, and respond to organizational risks and regulatory requirements.

---

## 🔐 3. Data Protection

### 🏷️ Sensitivity Labels
Used to classify and protect data.

Capabilities:
- Encryption (Azure Rights Management)
- Access restrictions (users/groups)
- Visual markings (headers, watermarks)
- Control printing, copying, and sharing

Example:
> “Confidential – HR Only” → accessible only to HR group

---

### 🚫 Data Loss Prevention (DLP)

Prevents sensitive data leakage across:

- Email (Outlook)
- Teams
- SharePoint / OneDrive
- Devices (via Defender for Endpoint)
- Copilot / AI interactions

Actions:
- Block
- Audit
- Allow with justification
- Notify users (policy tips)

Example:
- Block sending credit card data to external email

---

### 🧩 Information Protection

Combines:
- Manual labeling
- Automatic classification
- Policy enforcement
- Audit tracking

---

## 🧬 4. Data Classification

Purview identifies and classifies data using:

### 🔹 Sensitive Information Types (SITs)
Predefined patterns:
- Credit card numbers
- SSNs
- Passport numbers
- Health identifiers

Uses:
- Regex
- Checksum validation
- Keyword context

---

### 🤖 Trainable Classifiers
AI models trained with examples:

- Resumes
- Contracts
- Source code
- HR documents

Requires ~50+ samples to train custom classifiers.

---

### 🎯 Exact Data Match (EDM)

High-precision matching against internal datasets.

Example:
- Employee ID database
- Customer account numbers

👉 Unlike regex, EDM matches exact values → reduces false positives.

---

## ⏳ 5. Data Lifecycle Management (DLM)

Manages how long data is kept and when it is deleted.

### 🏷️ Retention Labels
- Retain data for a period
- Delete after expiration
- Retain + delete after lifecycle

Example:
> “7-Year Legal Hold”

---

### 📜 Retention Policies
Applied broadly across services:
- Exchange
- SharePoint
- Teams
- OneDrive

Used for baseline governance without user action.

---

### ⚙️ Auto-apply Rules
Automatically apply retention based on:
- Keywords
- Sensitive data types
- Classifiers

Example:
- Any document with credit card data → retain 5 years

---

## ⚠️ 6. Risk & Insider Threat Management

### 🕵️ Insider Risk Management

Detects abnormal behavior using:
- Machine learning
- HR signals
- Behavioral baselines

Examples:
- Mass file downloads
- Access outside working hours
- Data sent to personal email
- Activity during resignation period

---

### 📈 Activity Explorer

Provides forensic visibility:
- Timeline of user actions
- File access history
- Labeling events
- Sharing activity
- DLP triggers

---

### 💬 Communication Compliance

Monitors communication channels:

- Email
- Teams
- Yammer

Detects:
- Harassment
- Insider trading signals
- Policy violations

Includes:
- Reviewer dashboard
- Escalation workflows
- Machine learning + regex detection

---

## 📊 7. Compliance & eDiscovery

### 📌 Compliance Manager
Tracks regulatory compliance:

- GDPR
- HIPAA
- ISO 27001

Features:
- Compliance Score
- Assessments
- Improvement actions
- Control mapping

---

### 🔎 Data Explorer

Helps discover sensitive data:

- Where data is stored
- Who has access
- Exposure risk analysis

Filters:
- Location
- Sensitivity label
- Data type

---

### ⚖️ eDiscovery

Used for legal investigations:

#### Standard
- Search
- Export
- Legal hold

#### Premium
- Case management
- Review sets
- Analytics
- Redaction

Example:
- Preserve employee mailbox during legal case

---

## 🤖 8. AI Governance (Microsoft 365 Copilot + DSPM)

### 🧠 Copilot Data Model

Copilot:
- Does NOT access data directly
- Uses Microsoft Graph
- Inherits user permissions

👉 Key rule:
> Copilot only sees what the user can see

---

### 🌐 Microsoft Graph

Core data layer of Microsoft 365.

Functions:
- Secure API access layer
- Semantic search engine
- Context-aware retrieval

Includes:
- Identity-based access (OAuth)
- Temporal context (recent activity)
- Relationship mapping (people, files, teams)
- Semantic understanding (embeddings)

---

### 🔍 DSPM for AI (Data Security Posture Management)

Monitors AI usage:

- Detects AI access to sensitive data
- Tracks Copilot interactions
- Identifies shadow AI usage
- Classifies AI-generated content

Shadow AI = unauthorized use of AI tools outside IT control.

---

### 🧾 AI Risk Controls

- Prevent AI access to sensitive content
- Detect AI-generated confidential data
- Monitor external AI tools
- Apply DLP + labeling to AI outputs

---

### 📊 AI Reporting

- Activity Explorer for AI prompts
- Audit logs
- Oversharing detection
- Risk exposure reports

---

## 🌐 9. SharePoint Oversharing & Governance

### ⚠️ What is Oversharing?

Occurs when content is shared too broadly:

- “Anyone with the link”
- External guest access
- Edit permissions when not needed

---

### 🧨 Risks

- Data leaks
- Compliance violations
- Unauthorized access
- Loss of data control

---

### 🛠️ Detection Tools

- SharePoint Admin Center reports
- Microsoft 365 Admin Center
- PowerShell
- Microsoft Graph API
- Data Access Governance (DAG)

---

### 📌 DAG Reports

Identify:
- Overexposed sites
- Missing sensitivity labels
- Inactive owners
- External sharing risks

Actions:
- Revoke access
- Apply labels
- Restrict sharing

---

### 🏢 SharePoint Advanced Management (SAM)

Advanced controls:

- Restricted site access
- Inactivity alerts
- Access reviews
- Conditional Access integration

Example:
- Finance site accessible only from managed devices

---

## 🤝 10. Microsoft 365 Copilot Security Model

### 🔑 Key Principle

> Copilot is NOT a data source. It is a user-aware interface over Microsoft Graph.

---

### 🔐 Security Enforcement

Copilot respects:
- Sensitivity Labels
- DLP policies
- Conditional Access
- SharePoint permissions
- Entra ID identity model

---

### 📎 Sharing Behavior

- “Anyone with link” = accessible to Copilot
- Revoked link = access removed immediately

---

### 🛡️ Defender & Purview Integration

Admins can:
- Audit Copilot usage
- Monitor accessed content
- Detect policy violations
- Investigate AI interactions

---

## 🤖 11. Responsible AI Principles

Microsoft enforces:

### 📉 Data Minimization
Only necessary data is retrieved.

### 🔎 Transparency
Responses include source references.

### 🚫 Content Filtering
Blocks unsafe or inappropriate outputs.

### 📜 Auditability
All Copilot interactions are logged.

---

## 🧩 12. Final Summary

Microsoft Purview + Microsoft 365 ecosystem enables:

- Full data lifecycle governance
- Real-time risk detection
- AI-safe data usage
- Regulatory compliance automation
- Secure collaboration at scale

👉 Core idea:
> Data is only valuable if it is discoverable, protected, and governed — even in the era of AI.

---
