# Extended capabilities

**Purpose**: Test that the INSPIRE extended metadata is provided using the Metadata URL element or it is defined in the INSPIRE ExtendedCapabilities
XML Schema for ISO 19142.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* Check if the [ExtendedCapabilities](#extendedCapabilities) exists. If it does,

  * If [Metadata URL](#metadataURL) child node exists

    * Check if [Metadata URL](#metadataURL) is a valid URL.
  
  * Else

    * Check if [ExtendedCapabilities](#extendedCapabilities) element and it's children according to the XML Schema definition for the SOS INSPIRE extendedCapabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd

* If any of the checks or validations fails, the test fails

**Reference(s)**

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.6

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| ExtendedCapabilities <a name="extendedCapabilities"></a>   | ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1] |
| Metadata URL <a name="metadataURL"></a> | ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:MetadataUrl/inspire_common:URL |
