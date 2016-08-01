# Provide Response Language

**Purpose**: The Capabilities document must contain the response language

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/extended-capabilities)

**Test method**

* Check that [ResponseLanguage](#responseLanguage) exists. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirement 58

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
