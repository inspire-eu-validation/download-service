# Extended capabilities elements

**Purpose**: Test that the INSPIRE metadata is provided using the Metadata URL element or it is provided in the ExtendedCapabilities section.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* Check that the [ExtendedCapabilities](#extendedCapabilities) section exists. If it does,

  * If [Metadata Url](#metadataUrl) child node exists,

    * Check that [Metadata Url](#metadataUrl) is a valid URL.
  
  * Else

    * Check that the [ExtendedCapabilities](#extendedCapabilities) section contains all the mandatory INSPIRE metadata for the Download Service according with the schema "http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd".

* Check that all the mandatory elements that do not belong to the ExtendedCapabilities section shown in table 16 of [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs) are provided.

* If any of the checks or validations fails, the test fails.

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 6

**Test type**: Automated

**Notes**

The multiplicity of [ExtendedCapabilities](#extendedCapabilities) is 1.

The multiplicity of [Metadata Url](#metadataUrl) is 0 or 1.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| ExtendedCapabilities <a name="extendedCapabilities"></a>   | inspire_dls:ExtendedCapabilities |
| Metadata Url <a name="metadataUrl"></a> | inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL |
