# Awesome-Service-Automation-Business-Rules-Engine

# Awesome Service Automation & Business Rules Engine

> A curated list of top Service Automation and Business Rules Engine platforms — both SaaS/Hosted commercial solutions and open-source alternatives for automating business processes and encoding decision logic.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Camunda](#camunda)
  - [ServiceNow Flow Designer](#servicenow-flow-designer)
  - [Salesforce Flow](#salesforce-flow)
  - [Jira Automation](#jira-automation)
  - [Nintex](#nintex)
  - [Microsoft Power Automate](#microsoft-power-automate)
- [Open-Source Software](#-open-source-software)
  - [Drools (Apache KIE)](#drools-apache-kie)
  - [Flowable](#flowable)
  - [GoRules Zen Engine](#gorules-zen-engine)
  - [n8n](#n8n)
  - [Activepieces](#activepieces)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Service Automation and Business Rules Engine platforms. These are not open-source but are included as reference points for feature comparison.

### Camunda
**Type:** Enterprise BPMN/DMN process and decision automation  
Camunda provides a flexible framework for workflow and decision automation with BPMN and DMN, with integration for Quarkus, Spring, Spring Boot, and CDI [citation:3]. It is the commercial standard for organizations needing standards-based process orchestration with a visual modeler and execution engine. The platform is widely used for service automation where both human tasks and automated rules must be coordinated.

### ServiceNow Flow Designer
**Type:** Platform-native workflow orchestration  
ServiceNow Flow Designer enables automation within the ServiceNow platform, allowing teams to build flows that react to record changes, schedules, and external events. It is the natural choice for organizations already using ServiceNow for ITSM or CSM, as flows operate directly on platform data without external integration overhead.

### Salesforce Flow
**Type:** Declarative automation within Salesforce  
Salesforce Flow provides visual automation for record-triggered, screen-based, and scheduled workflows inside the Salesforce platform. It is the standard for Salesforce-centric organizations needing to automate business logic across Sales, Service, and custom objects without external tooling.

### Jira Automation
**Type:** Rule-based automation within Atlassian ecosystem  
Jira Automation allows teams to create trigger-condition-action rules that automate issue transitions, notifications, and field updates. It is the default choice for software teams already using Jira for project tracking, with no additional platform needed for basic workflow rules.

### Nintex
**Type:** Visual workflow automation with forms and document generation  
Nintex provides workflow automation with forms, document generation, and process intelligence. It is often used for approval workflows and contract-related processes, with integrations into SharePoint and Office 365.

### Microsoft Power Automate
**Type:** Low-code automation across Microsoft ecosystem  
Power Automate enables business users to build workflows with a visual designer and hundreds of connectors. It is best suited for organizations already standardized on Microsoft 365, where flows can be embedded into SharePoint, Teams, and Dynamics surfaces.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Service Automation and Business Rules Engine tools. The open-source ecosystem spans **business rules engines** for decision logic and **workflow automation platforms** for process orchestration.

### Drools (Apache KIE)
**Stack:** Java | **License:** Apache-2.0  
Drools is a business rule management system with forward-chaining and backward-chaining inference, supporting DRL, DMN, and Decision Table spreadsheets in Excel format [citation:4][citation:12]. It is part of the Apache KIE (incubating) umbrella, which also includes jBPM for BPMN 2.0 processes and OptaPlanner for constraint solving [citation:6]. Drools includes a complex event processing (CEP) engine for detecting patterns in event streams, useful for fraud detection and IoT scenarios [citation:12]. Rules can be authored as source code or as decision tables, making them accessible to business users. The engine is the most established open-source business rules engine, with decades of production use.
**Best for:** Java teams needing a mature, inference-based rules engine with DMN decision tables and complex event processing, accepting the learning curve of DRL/FEEL syntax.

### Flowable
**Stack:** Java | **License:** Apache-2.0  
Flowable provides open-source BPMN, CMMN, and DMN engines that are compact and highly efficient, capable of running embedded in a Java application or as a service on a server, cluster, or cloud [citation:5]. The engines are Apache-2.0 licensed with a committed community (5k+ GitHub stars) [citation:5]. Flowable's rules/decision engine uses a dedicated model for optimized DMN execution, while the process engine handles BPMN orchestration and the case engine handles CMMN [citation:5]. Rich Java and REST APIs make it suitable for orchestrating both human and automated processing. The enterprise edition adds an Agentic Case Platform for governing AI agents alongside people and processes [citation:5].
**Best for:** Teams wanting a modern, Apache-licensed process and decision engine with BPMN, CMMN, and DMN support, accepting the operational overhead of a Java-based platform.

### GoRules Zen Engine
**Stack:** Rust / Go / Node.js / Python | **License:** Open Source (per project)  
GoRules Zen Engine is a lightweight, embeddable business rules engine that evaluates decision tables and graphs, with bindings for Rust, Go, Node.js, and Python [citation:1][citation:9]. Decision tables are evaluated row by row with configurable hit policies (`first` or `collect`), and inputs support unary tests (equality, numeric comparisons, ranges) or expression evaluation using the ZEN Expression Language [citation:1]. The JDM (JSON Decision Model) graph supports Decision Table, Switch, Function, and Expression nodes, with an Input node for data and Output node for results [citation:9]. A free online editor with built-in simulator is available. This is a focused rules engine rather than a full workflow platform.
**Best for:** Developers wanting an embeddable, multi-language decision engine for evaluating business rules without the overhead of a full BPM platform, particularly for service-level pricing or eligibility logic.

### n8n
**Stack:** TypeScript / Node.js | **License:** Sustainable Use (source-available)  
n8n is the most widely adopted source-available workflow automation platform, with a visual builder and 400+ integrations, plus JavaScript/Python code nodes for custom logic [citation:15]. It supports self-hosting for full data control and is popular with technical teams building AI-enhanced business automations [citation:15]. **Important:** The Sustainable Use License is source-available but not OSI-approved open source, though internal self-hosting is permitted. For service automation, n8n can trigger workflows from webhooks, schedules, or app events, and chain actions across systems.
**Best for:** Technical teams wanting a powerful, self-hostable automation platform with broad app coverage and AI capabilities, accepting the source-available licensing terms.

### Activepieces
**Stack:** TypeScript | **License:** MIT  
Activepieces is a genuinely MIT-licensed open-source automation platform positioned as a permissively licensed alternative to n8n, with 500+ integrations and a visual builder [citation:15]. The MIT license allows full commercial use and modification, making it suitable for embedding in products or white-labeling. The platform supports both no-code and code customization, with a growing community (60% of integrations built by users) [citation:15]. **Trade-off:** Fewer integrations than n8n or Zapier, and a smaller community, but the permissive license is a key differentiator for teams that cannot accept source-available terms.
**Best for:** Teams wanting an MIT-licensed, self-hostable automation platform without the restrictions of source-available licenses, accepting a smaller integration library.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Rules Engine | Workflow Automation | Self-Hosted | Best For |
|----------|---------|-------|--------------|---------------------|-------------|----------|
| **Camunda** | Proprietary | Java | ✅ DMN | ✅ BPMN | (Self-Managed) | Enterprise BPMN/DMN |
| **ServiceNow** | Proprietary | Cloud | (Platform) | ✅ Flow Designer | ❌ | ServiceNow platform |
| **Salesforce Flow** | Proprietary | Cloud | (Platform) | ✅ Visual flows | ❌ | Salesforce platform |
| **Power Automate** | Proprietary | Cloud | (Platform) | ✅ Low-code | ❌ | Microsoft 365 |
| **Drools** | Apache-2.0 | Java | ✅ Inference + DMN | (Via jBPM) | ✅ | Mature rules engine |
| **Flowable** | Apache-2.0 | Java | ✅ DMN | ✅ BPMN/CMMN | ✅ | Modern process + decision |
| **GoRules Zen** | Open Source | Multi | ✅ Decision tables | ❌ (Embeddable) | ✅ (Library) | Embeddable rules |
| **n8n** | Sustainable Use | TypeScript | ❌ | ✅ Visual | ✅ | Broad automation + AI |
| **Activepieces** | MIT | TypeScript | ❌ | ✅ Visual | ✅ | MIT-licensed automation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Service Automation or Business Rules Engine that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note if it is source-available but not OSI-approved, as with n8n). Note that the open-source ecosystem **splits** between **business rules engines** (Drools, Flowable DMN, GoRules Zen) for decision logic and **workflow automation platforms** (n8n, Activepieces) for process orchestration. **Drools** is the most mature open-source rules engine with inference and CEP capabilities [citation:12]. **Flowable** offers the strongest combined BPMN/CMMN/DMN stack under Apache-2.0 [citation:5]. **GoRules Zen** is notable for embeddability across multiple languages [citation:1]. For visual automation, **Activepieces** is the MIT-licensed choice while **n8n** offers broader integrations under a source-available license [citation:15].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
