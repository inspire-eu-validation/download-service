# A.06.IR223.TGR58.provideResponseLanguage

**Purpose**: The Capabilities document must contain the response language

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET
* [A.01.TGR60.extended.capabilities](A.01.TGR60.extended.capabilities.md)

**Test method**

* Check that [ResponseLanguage](#responseLanguage) exists. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* TG, Req 58
* IR, Section 2.2.3

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
