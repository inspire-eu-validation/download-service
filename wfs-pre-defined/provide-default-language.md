# Provide Default Language

**Purpose**: The Capabilities document must contain the default language.

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/extended-capabilities)

**Test method**

* Check that the [DefaultLanguage](#defaultLanguage) exists. Let it's value be ```default-language```.
* Perform a GetCapabilities request for the same service without the LANGUAGE-parameter. Let the response document be ```doc-1```. The [ResponseLanguage](#responseLanguage) of ```doc-1``` must be equal to the ```default-language```.
* Perform a GetCapabilities request for the same service with the LANGUAGE-parameter set to some non-empty value not in [supported language codes](#supported-languges). Let the response document be ```doc-2```. The [ResponseLanguage](#responseLanguage) of Let the response document be ```doc-2```. must be equal to the ```default-language```.
* Test that the values of each [Title](#title) and [Abstract](#abstract) elements in ```doc-1``` and ```doc-2``` are identical.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirement 57

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DefaultLanguage <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
Supported language codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
Title <a name="title"></a> | //\*:Title
Abstract <a name="abstract"></a> | //\*:Abstract
