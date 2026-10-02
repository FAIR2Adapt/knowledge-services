# Multilingual Generative Question Answering in CCA

<!-- Multilingual generative question answering - from D4.1 V_41, Section 3.3.1 (Table 4: WP4-T43-S1, Expert.ai) -->
## 1. Multilingual generative question answering

<p class="svc-meta">Service ID WP4-T43-S1 · Partner Expert.ai · D5.3 user stories F2A-CS4-US2, F2A-CS5A-US2</p>

A multilingual AI-powered assistant that helps users explore and understand climate change adaptation knowledge by providing conversational answers based on trusted information resources. The service provides multilingual question-answering capabilities in the climate change adaptation domain. It retrieves relevant information from a dedicated knowledge base and generates natural-language responses using generative AI. The knowledge base was initially created from a compilation of research articles, and it can be extended with other sources. Users can ask follow-up questions within the same conversation, and the service is available through both a web interface and an API endpoint.

| **Category** | **Field** | **Description** |
|:---|:---|:---|
| **Technical Specification** | **Inputs** | Question in plain text. |
| | **Outputs** | Answer in plain text. |
| | **Data Format** | Plain text |
| | **Target User Groups** | Users exploring climate change adaptation knowledge (web interface and API). |
| | **Access Specification** | API: [chat completions endpoint](https://docs.openwebui.com/reference/api-endpoints/#-chat-completions) |
| **Data & Resources** | **Data Source(s)** | A dedicated knowledge base compiled from research articles, extensible with other sources. |
| | **Interacting with available F2A APIs** | <li> <a href="https://www.rohub.org/">ROHub</a>: RO-Crate related APIs </li> |

---

<!-- PYTHIA (KGQA) - from D4.1 V_41, Section 3.1.4; Table 4 lists it as WP4-T43-S2 under T4.3 -->
## 2. PYTHIA (KGQA)

<p class="svc-meta">Service ID WP4-T43-S2 · D5.3 user stories F2A-CS4-US5, F2A-CS5A-US2</p>

PYTHIA is a knowledge graph question-answering (KGQA, Text-to-SPARQL) engine that is designed to function as a plug-and-play solution for general-purpose and specialized knowledge graphs (KG), without requiring any fine-tuning or KG-specific modification.

| **Category** | **Field** | **Description** |
|:---|:---|:---|
| **Technical Specification** | **Inputs** | <ul><li>For the engine's deployment: target knowledge graph, made available both as an endpoint and as source files.</li><li>During inference: user query in natural language.</li></ul> |
| | **Outputs** | SPARQL query result set. |
| | **Data Format** | Natural-language query in; SPARQL result set out. |
| | **Target User Groups** | Users querying a knowledge graph in natural language. |
| | **Access Specification** | Package repository: [github.com/SKefalidis/PYTHIA](https://github.com/SKefalidis/PYTHIA/) |
| **Data & Resources** | **Data Source(s)** | The target knowledge graph (endpoint and source files). |
| | **Interacting with available F2A APIs** | <li> <a href="https://www.rohub.org/">ROHub</a>: RO-Crate related APIs </li> |
