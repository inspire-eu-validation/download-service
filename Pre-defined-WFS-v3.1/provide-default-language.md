# Provide Default Language

**Purpose**: The Capabilities document must contain the default language.

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET
* [Extended capabilities](extended-capabilities.md)

**Test method**

* Check that the [DefaultLanguage](#defaultLanguage) exists. Let it's value be ```default-language```.
* Perform a GetCapabilities request for the same service without the LANGUAGE-parameter. Let the response document be ```doc-1```. The [ResponseLanguage](#responseLanguage) of ```doc-1``` must be equal to the ```default-language```.
* Perform a GetCapabilities request for the same service with the LANGUAGE-parameter set to some non-empty value not in [supported language codes](#supported-languges). Let the response document be ```doc-2```. The [ResponseLanguage](#responseLanguage) of Let the response document be ```doc-2```. must be equal to the ```default-language```.
* Test that the values of each [Title](#title) and [Abstract](#abstract) elements in ```doc-1``` and ```doc-2``` are identical.

**Reference(s)**:

* TG, Req 59

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DefaultLanguage <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
Supported language codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
Title <a name="title"></a> | //\*:Title
Abstract <a name="abstract"></a> | //\*:Abstract
