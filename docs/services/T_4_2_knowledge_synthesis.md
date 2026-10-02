# FDO Services for Knowledge Synthesis in CCA

The service's purpose is to develop a framework for data and knowledge integration and synthesis, addressing the challenge of combining information from different disciplines and sources relevant to Climate Change Adaptation (CCA).

<!-- TIB Knowledge Loom Service - from D4.1 V_41, Section 3.2.1 (Table 4: WP4-T42-S1, TIB) -->
## 1. TIB Knowledge Loom

<p class="svc-meta">Service ID WP4-T42-S1 · Partner TIB · D5.3 user stories F2A-CS3-US3, F2A-CS6-US4</p>

FAIR2Adapt's knowledge-production layer turns case-study findings into machine-readable knowledge that is reusable from the outset. FAIR2Adapt delivers this as the TIB Knowledge Loom, building on ORKG-reborn. Where a finding and the data, code and figures behind it are only loosely connected, it becomes difficult to tell which evidence supports a given statement, how a result was produced, and whether it can be reused in another workflow. The service addresses this by creating structured, machine-readable knowledge records: each scientific statement is linked to its supporting evidence, including input data, software code, generated figures, workflow outputs, provenance information and the related RO-Crate metadata. A knowledge record therefore describes a result together with the data and processes that support it, serialised as a JSON-LD graph and packaged as an RO-Crate. The knowledge-organisation layer turns deposited artifacts into a persistent knowledge graph in which Loom records, scientific statements, evidence objects, relations and collections are typed and individually addressable; this graph is the data model the Knowledge Loom services operate on.

| **Category** | **Field** | **Description** |
|:---|:---|:---|
| **Technical Specification** | **Inputs** | <ul><li>Research article.</li><li>Supporting datasets and access specification, model outputs or processed data.</li><li>Source code, scripts, software methods or workflow steps.</li></ul> |
| | **Outputs** | <ul><li>Machine-readable scientific statements.</li><li>Evidence records linking statements to data, code, figures, methods and outputs.</li><li>Typed, directed relations between statements (e.g. supports).</li><li>Collections that group related records and statements.</li><li>Persistent identifiers (DataCite DOIs) for both records and statements.</li><li>Knowledge records serialised as JSON-LD and packaged as RO-Crate FAIR Digital Objects, deposited in a repository and publishable through project infrastructures such as ROHub.</li><li>User-facing evidence views.</li></ul> |
| | **Data Format** | RO-Crate in JSON-LD |
| | **Target User Groups** | Researchers and policymakers |
| | **Access Specification** | UI: [knowledgeloom.tib.eu](https://knowledgeloom.tib.eu/)<br>API: [API Specification](./api_specification/T_4_2_swagger_ui.html)<br>Repository: [gitlab.com/TIBHannover/lki/knowledge-loom/loom-backend](https://gitlab.com/TIBHannover/lki/knowledge-loom/loom-backend) |
| **Data & Resources** | **Data Source(s)** | Structured knowledge harvested from narrative text documents (scientific articles and reports). |
| | **Interacting with available F2A APIs** | <ul><li>[Connectivity Hub](https://connectivity-hub.weadapt.org/about): Using it for having a shared vocabulary and hierarchical structure to describe a knowledge domain<ul><li>[Taxonomy API Documentation](https://connectivity-hub.com/)</li></ul></li><li>[ROHub](https://www.rohub.org/): RO-Crate related APIs<ul><li>[ROHub API documentation](https://reliance-eosc.github.io/rohub-portal-documentation/)</li></ul></li></ul> |
