# Extended capabilities

**Purpose**: The INSPIRE extended metadata is provided using the elements defined in the INSPIRE ExtendedCapabilities
XML Schema for ISO 19142. The purpose of this test is to verify that the INSPIRE ExtendedCapabilities root element
is included in the WFS GetCapabilities responsem and that the contents of the root element are valid according to the
XML Schema for the INSPIRE WFS ExtendedCapabilities.

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET

**Test method**

* Check that the [ExtendedCapabilities](#ExtendedCapabilities) exists. If it does
  * Validate the [ExtendedCapabilities](#ExtendedCapabilities) element and it's children according to the XML Schema definition for the WFS INSPIRE extendedCapabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
  * If the validation passes, pass the test.
* If no ExtendedCapabilities were found or validation fails, fail the test.

**Reference(s)**

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]
