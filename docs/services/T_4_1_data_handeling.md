<!-- ### T4.1. FDO Services interfaces for data handling in CCA -->
<!--A high-level, non-technical description of what the service will do.-->

<!-- # T.4.1.1 Data Handling — Layman - inserted by Milos Ulman, Plan4All -->
# T.4.1.1 Data Handling — Layman

## Conceptual Specification  
**Layman** is an open-source geospatial publication service developed by the [LayerManager project](https://github.com/LayerManager/layman).  
It enables users to **upload, style, manage, and publish** spatial datasets as FAIR-compliant digital resources.  

Within the broader **[Hub4Everybody](https://hub4everybody.eu/)** platform, Layman acts as the spatial-data publication component, allowing users to ingest, visualize, and share geographic layers and maps.  
In the context of **FAIR2ADAPT**, Layman supports the *data handling and publication* stage of the FAIRification process — enabling transformation of geospatial data into interoperable and reusable FAIR Digital Objects (FDOs).

---

**Core Functionality:** Layman provides services for:  
- **Ingestion** of geospatial data (vector and raster) through API or web interface.  
- **Styling and visualization** using standard symbology formats (SLD, Symbology Encoding, QGIS style).  
- **Publication** as OGC-compliant web services (WMS, WFS) and catalogue entries (CSW).  
- **Metadata management** including ownership, provenance, and access rights.  
- **Map composition** enabling aggregation of multiple layers into one reusable entity.  
- **Access control and authentication** including OAuth2 integration.  

Layman supports synchronous and asynchronous workflows, with chunked uploads for large datasets, ensuring scalability for complex geospatial resources.

---

**Input Data:** 
- **Vector formats**: GeoJSON, Shapefile, PostGIS tables.  
- **Raster formats**: GeoTIFF, JPEG2000, PNG, JPEG.  
- **Style definitions**: SLD, Symbology Encoding, QGIS style files.  
- **Map compositions**: HSLayers Map Composition JSON format.  
- **Metadata**: Automatically generated or user-defined; compliant with OGC CSW specifications.

---

**Output Data:** 
- **Published Layers**: Accessible through REST API, WMS, and WFS.  
- **Published Maps**: Composite sets of layers available for embedding or sharing.  
- **Catalogue Metadata**: Exposed via CSW service, enabling findability and machine discoverability.  
- **FAIR Digital Objects (Spatial)**: Machine-actionable resources ready for integration within FAIR2ADAPT workflows.

---

## Technical Specification  

| **Category** | **Field** | **Description** |
|---------------|------------|-----------------|
| **Technical Specification** | **Data Format** | Vector (GeoJSON, Shapefile, PostGIS), Raster (GeoTIFF, JPEG2000, PNG, JPEG), Styles (SLD, QGIS Style), Map Compositions (HSLayers). |
| | **Target User Groups**  | Geospatial data providers, research infrastructures, data managers, and FAIR2ADAPT users requiring spatial data publication and FAIR integration. |
|  | **API Specification URL** | [Layman REST API](https://github.com/LayerManager/layman/blob/master/doc/rest.md) |
| **Data & Resources** | **Data Source(s)** | Data uploaded by users or harvested from connected geospatial databases (e.g., PostGIS). |
|  | **Interacting with available F2A APIs** | Layman exposes spatial layers and maps to other FAIR2ADAPT services (e.g., ROHub) via OGC CSW/WMS endpoints or custom connectors. Integration enables inclusion of Layman-published resources as FAIR Digital Objects within the FAIR2ADAPT ecosystem. |

<!-- # T.4.1.2 Data Handling — Micka - inserted by Milos Ulman, Plan4All -->
# T.4.1.2 Data Handling — Micka

## Conceptual Specification  
Micka is a metadata catalogue application for the management, publication, and discovery of spatial-data and spatial-service metadata. It supports key standards (ISO 19115/19119/19110, INSPIRE) and exposes OGC CSW endpoints for interoperable metadata discovery.  
Within the Hub4Everybody ecosystem, Micka acts as the metadata‐catalogue component, enabling users to register, edit, harvest, and publish metadata records for datasets, services, and derived resources. In the context of the FAIRification Framework, Micka supports the *design → implementation → deployment* phases by transforming metadata into FAIR digital objects ready for discovery and reuse.

---

**Core Functionality:**  
Micka provides the following core services:  
- Metadata ingestion via manual editing, import (XML/ISO profiles) or harvesting from external services.  
- Metadata editing and management with configurable metadata profiles (e.g., ISO 19115 core/full, INSPIRE, custom). :contentReference[oaicite:3]{index=3}  
- Metadata discovery via OGC CSW 2.0.2 (ISO AP1.0) endpoint, supporting search, pagination and advanced query criteria. :contentReference[oaicite:4]{index=4}  
- Support for multilingual metadata, custom profiles, and export in various formats (XML/JSON/RDF) for interoperability. :contentReference[oaicite:5]{index=5}  
- Administration and role-based access: administrators handle configuration, harvesting modules and editing rights. :contentReference[oaicite:6]{index=6}  

---

**Input Data:** 
- Metadata records in ISO 19115/19119/19110, Dublin Core (ISO 15836) and custom profiles. :contentReference[oaicite:7]{index=7}  
- Harvested metadata from external CSW or other OGC services.  
- Manually entered metadata via user interface, or imported from XML/ISO files. :contentReference[oaicite:8]{index=8}  
- Multilingual metadata input (UTF-8) and configurable metadata profiles for provider-specific needs.

---

**Output Data:**  
- Public metadata catalogue exposed via OGC CSW endpoint (queryable by client applications). 
- Export of metadata records in formats such as XML (ISO), JSON, GeoDCAT, RDFa for machine-readability and reuse. :contentReference[oaicite:9]{index=9}  
- Metadata records ready to function as FAIR Digital Objects within the FAIR2ADAPT ecosystem: discoverable, accessible, interoperable, reusable.

---

## Technical Specification  

| **Category** | **Field** | **Description** |
|-------------|-----------|-----------------|
| Technical Specification | Data Format | Metadata formats: ISO 19115/19119/19110, Dublin Core (ISO 15836), custom profiles; export formats: XML, JSON, RDFa. |
|  | Target User Groups | Metadata managers, data cataloguers, spatial data service providers, research infrastructures, FAIR2ADAPT users wanting to register and expose metadata for geospatial resources. |
| | API Specification URL | (CSW endpoint; documentation accessible via Micka documentation site) |
| Data & Resources | Data Source(s) | Metadata supplied by data/service owners, harvested from external CSW/OGC services, imported from XML/ISO files. |
|  | Interacting with available F2A APIs | Micka exposes metadata as CSW services which can be ingested by other FAIR2ADAPT components (e.g., resource hubs, discovery portals) and supports linking with other catalogues or datasets in the Hub4Everybody framework. |

---
