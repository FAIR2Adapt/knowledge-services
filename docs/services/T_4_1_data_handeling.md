# FDO Services Interfaces for Data Handling in CCA

<!-- Services in this family: Layman (WP4-T41-S1), Micka (WP4-T41-S2), dtreg (WP4-T41-S4) — content from D4.1 V_41, Section 3.1 -->

## 1. Layman

<p class="svc-meta">Service ID WP4-T41-S1 · Partner P4A, Lesprojekt · D5.3 user stories F2A-CS2-US2, F2A-CS2-US3, F2A-CS2-US4</p>

**Layman** is an open-source geospatial publication service developed by the [LayerManager project](https://github.com/LayerManager/layman).  It enables users to upload, style, manage, and publish spatial datasets as FAIR-compliant digital resources. Within the broader **[Hub4Everybody](https://hub4everybody.eu/)** platform, Layman acts as the spatial-data publication component, allowing users to ingest, visualize, and share geographic layers and maps.  
In the context of FAIR2ADAPT, Layman supports the *data handling and publication* stage of the FAIRification process — enabling transformation of geospatial data into interoperable and reusable FAIR Digital Objects (FDOs). 

| **Category** | **Field** | **Description** |
|---------------|------------|-----------------|
| **Technical Specification** | **Inputs** | <ul><li>Vector formats: GeoJSON, Shapefile, PostGIS tables.</li><li>Raster formats: GeoTIFF, JPEG2000, PNG, JPEG.</li><li>Style definitions: SLD, Symbology Encoding, QGIS style files.</li><li>Map compositions: HSLayers Map Composition JSON format.</li><li>Metadata: automatically generated or user-defined; compliant with OGC CSW specifications.</li><li>RO-Crate FDO: [w3id.org/ro-id/9c8ee58c-28f8-42ad-9ba8-0daf91935d31](https://w3id.org/ro-id/9c8ee58c-28f8-42ad-9ba8-0daf91935d31)</li></ul> |
| | **Outputs** | <ul><li>Published Layers: accessible through REST API, WMS, and WFS.</li><li>Published Maps: composite sets of layers available for embedding or sharing.</li><li>Catalogue Metadata: exposed via CSW service, enabling findability and machine discoverability.</li><li>FAIR Digital Objects (Spatial): machine-actionable resources ready for integration within FAIR2ADAPT workflows.</li></ul> |
| | **Target User Groups** | Geospatial data providers, research infrastructures, data managers, and FAIR2ADAPT users requiring spatial data publication and FAIR integration. |
| | **Access Specification** | UI: [f2a.plan4all.eu/#…9c8ee58c](https://f2a.plan4all.eu/#https://w3id.org/ro-id/9c8ee58c-28f8-42ad-9ba8-0daf91935d31)<br>API: [f2a.plan4all.eu/?url=…2473e95d](https://f2a.plan4all.eu/?url=https://w3id.org/ro-id/2473e95d-0425-4041-96e0-316a5fc2d71d) · [Layman REST API](https://github.com/LayerManager/layman/blob/master/doc/rest.md)<br>Package: [github.com/FAIR2Adapt/riomar-dashboard](https://github.com/FAIR2Adapt/riomar-dashboard) |
| **Data & Resources** | **Data Source(s)** | - |
|  | **Interacting with available F2A APIs** | Layman exposes spatial layers and maps to other FAIR2ADAPT services (e.g., ROHub) via OGC CSW/WMS endpoints or custom connectors. Integration enables inclusion of Layman-published resources as FAIR Digital Objects within the FAIR2ADAPT ecosystem. |

---

## 2. Micka

<p class="svc-meta">Service ID WP4-T41-S2 · Partner P4A</p>

Micka is a metadata catalogue application for the management, publication, and discovery of spatial-data and spatial-service metadata. It supports key standards (ISO 19115/19119/19110, INSPIRE) and exposes OGC CSW endpoints for interoperable metadata discovery.  
Within the Hub4Everybody ecosystem, Micka acts as the metadata‐catalogue component, enabling users to register, edit, harvest, and publish metadata records for datasets, services, and derived resources. In the context of the FAIRification Framework, Micka supports the *design → implementation → deployment* phases by transforming metadata into FAIR digital objects ready for discovery and reuse.

| **Category** | **Field** | **Description** |
|-------------|-----------|-----------------|
| **Technical Specification** | **Inputs** | <ul><li>Metadata records in ISO 19115/19119/19110, Dublin Core (ISO 15836) and custom profiles.</li><li>Harvested metadata from external CSW or other OGC services.</li><li>Manually entered metadata via user interface, or imported from XML/ISO files.</li><li>Multilingual metadata input (UTF-8) and configurable metadata profiles for provider-specific needs.</li></ul> |
| | **Outputs** | <ul><li>Public metadata catalogue exposed via OGC CSW endpoint (queryable by client applications).</li><li>Export of metadata records in formats such as XML (ISO), JSON, GeoDCAT, RDFa for machine-readability and reuse.</li><li>Metadata records ready to function as FAIR Digital Objects within the FAIR2ADAPT ecosystem: discoverable, accessible, interoperable, reusable.</li></ul> |
| | **Data Format** | Metadata formats: ISO 19115/19119/19110, Dublin Core (ISO 15836), custom profiles; export formats: XML, JSON, RDFa. |
| | **Target User Groups** | Metadata managers, data cataloguers, spatial data service providers, research infrastructures, FAIR2ADAPT users wanting to register and expose metadata for geospatial resources. |
| | **Access Specification** | UI: [github.com/hsrs-cz/Micka](https://github.com/hsrs-cz/Micka)<br>API: TBD (CSW endpoint; documentation on the Micka documentation site)<br>Package: [Micka v2020.015](https://github.com/hsrs-cz/Micka/releases/tag/v2020.015) |
| **Data & Resources** | **Data Source(s)** | Metadata supplied by data/service owners, harvested from external CSW/OGC services, imported from XML/ISO files. |
|  | **Interacting with available F2A APIs** | Micka exposes metadata as CSW services which can be ingested by other FAIR2ADAPT components (e.g., resource hubs, discovery portals) and supports linking with other catalogues or datasets in the Hub4Everybody framework. |

---

## 3. dtreg

<p class="svc-meta">Service ID WP4-T41-S4 · Partner TIB · D5.3 user stories F2A-CS3-US3, F2A-CS6-US4</p>

dtreg allows researchers to describe an analysis directly in Python or R using registered ePIC or ORKG schemata. Once the schema-related object is populated, the description is serialised as JSON-LD, creating a lightweight machine-readable representation of the analysis. The TIB Knowledge Loom uses this service, and a record produced this way has been validated with roc-validator and ingested into ROHub, establishing the exchange path for future deposition and harvesting between these services.

| **Category** | **Field** | **Description** |
|-------------|-----------|-----------------|
| **Technical Specification** | **Inputs** | <ul><li>Data analysis method</li><li>Metadata about software/method</li><li>Input data description</li><li>Output/results of analysis</li><li>Scientific statement (optional)</li><li>ePIC/ORKG schema</li></ul> |
| | **Outputs** | <ul><li>Machine-readable JSON-LD description</li><li>Structured metadata for method</li><li>FAIR-compatible linked data</li><li>Reusable record for Knowledge Loom</li></ul> |
| | **Data Format** | JSON-LD (serialised from ePIC/ORKG schemata); Python and R packages. |
| | **Target User Groups** | Researchers |
| | **Access Specification** | Package: [pypi.org/project/dtreg](https://pypi.org/project/dtreg) |
| **Data & Resources** | **Data Source(s)** | Analysis descriptions provided by the researcher; registered ePIC/ORKG schemata. |
|  | **Interacting with available F2A APIs** | Records are used by the TIB Knowledge Loom; a record has been validated with roc-validator and ingested into [ROHub](https://www.rohub.org/). |
