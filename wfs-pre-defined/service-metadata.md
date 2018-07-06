# Service Metadata

**Purpose**:
INSPIRE Metadata for the Download Service must EITHER be linked to via an [inspire_common:MetadataURL](#inspireCommonMetadataUrl) in an [ExtendedCapabilities](#ExtendedCapabilities) section, OR the [ExtendedCapabilities](#ExtendedCapabilities) section must contain all the INSPIRE Metadata for the Download Service in accordance with Table 4 and the inspire_dls:ExtendedCapabilities schema.

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/extended-capabilities)

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
* Check if all mandatory metadata elements as specified in Table 19 of the TG exist in the [ExtendedCapabilities](#ExtendedCapabilities) section.
* If a [inspire_common:MetadataURL](#inspireCommonMetadataUrl) is provided, request the Metadata document with this URL. Check if the response is a valid Metadata document.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirement 53, Table 19

**Test type**:

Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
inspire_common:MetadataURL <a name="inspireCommonMetadataUrl"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL
