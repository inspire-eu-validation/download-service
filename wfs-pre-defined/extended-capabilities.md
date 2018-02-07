# Extended capabilities

**Purpose**: The INSPIRE extended metadata is provided using the elements defined in the INSPIRE ExtendedCapabilities
XML Schema for ISO 19142. The purpose of this test is to verify that the INSPIRE ExtendedCapabilities root element
is included in the WFS GetCapabilities response and that the contents of the root element are valid according to the
XML Schema for the INSPIRE WFS ExtendedCapabilities.

**Prerequisites**

**Test method**

* Check that the [ExtendedCapabilities](#ExtendedCapabilities) exists. If it does
  * Validate the [ExtendedCapabilities](#ExtendedCapabilities) element and its children according to the XML Schema definition for the WFS INSPIRE ExtendedCapabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
  * If the validation passes, pass the test.
* If no ExtendedCapabilities were found or validation fails, fail the test.

**Reference(s)**

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirement 60

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]
