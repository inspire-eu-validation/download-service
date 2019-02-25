# Extended capabilities

**Purpose**: Test that the INSPIRE extended metadata is provided using the Metadata URL element or it is defined in the INSPIRE ExtendedCapabilities
XML Schema for ISO 19142.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* Check if the [ExtendedCapabilities](#extendedCapabilities) exists. If it does,

  * If [Metadata Url](#metadataUrl) child node exists,

    * Check if [Metadata Url](#metadataUrl) is a valid URL.
  
  * Else

    * Check if the [ExtendedCapabilities](#extendedCapabilities) section contains all the mandatory INSPIRE metadata for the Download Service according with the schema "http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd".

* Check if all the mandatory elements that do not belong to the ExtendedCapabilities section shown in table 13 of [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0) are provided.

* If any of the checks or validations fails, the test fails.

**Reference(s)**

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.6

**Test type**: Automated

**Notes**

The multiplicity of [ExtendedCapabilities](#extendedCapabilities) is 1.

The multiplicity of [Metadata Url](#metadataUrl) is 0 or 1.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| ExtendedCapabilities <a name="extendedCapabilities"></a>   | inspire_dls:ExtendedCapabilities |
| Metadata Url <a name="metadataUrl"></a> | inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL |
