# A.07.IR223.TGR59.provideSupportedLanguages

**Purpose**: The Capabilities document must contain a list of supported languages

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET
* [A.01.TGR60.extended.capabilities](A.01.TGR60.extended.capabilities.md)

**Test method**

* Check that the [Supported language codes](#supported-languages) list is non-empty. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* TG, Req 59
* IR, Section 2.2.3

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Supported language codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
