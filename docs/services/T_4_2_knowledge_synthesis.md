<!-- ### FDO Services for Transdisciplinary Knowledge Synthesis in CCA -->
The service's purpose is to develop framework for data and knowledge integration and synthesis, addressing the challenge of combining information from different disciplines and sources relevant to Climate Change Adaptation (CCA).

## Conceptual Specification

**Core Functionality:** This service will harvest structured knowledge from sources like scientific articles, government reports, and knowledge graphs to provide a unified platform for knowledge synthesis.

**Input Data:** The API endpoints accept inputs based on API functinality, for example retrival APIs need to recive inputs like article and dataset identifiers to retrieve data.

**Output Data:** The API's outputs are RO-Crates that includes metadata about the source. This crate contains scientific statements and their supporting evidence in a machine-readable JSON-LD format.


## Technical Specification

| **Category** | **Field** | **Description** |
|:---|:---|:---|
| **Technical Specification** | **Data Format** | RO-Crate in JsonLD |
| | **Target User Groups** | Researchers and policymakers |
| | **API Specification URLs ** | [API Specification](./api_specification/T_4_2_swagger_ui.html) |
| **Data & Resources** | **Data Source(s)** | Structured knowledge harvested from narrative text documents (scientific articles and reports). |
| | **Interacting with available F2A APIs** | <ul><li>[Connectivity Hub](https://connectivity-hub.weadapt.org/about): Using it for having a shared vocabulary and hierarchical structure to describe a knowledge domain<ul><li>[Taxonomy API Documentation](https://connectivity-hub.com/)</li></ul></li><li>[ROHub](https://www.rohub.org/): RO-Crate related APIs<ul><li>[ROHub API documentation](https://reliance-eosc.github.io/rohub-portal-documentation/)</li></ul></li></ul> |