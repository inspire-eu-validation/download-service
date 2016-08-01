# Language affects capabilities

**Purpose**: The user must be able to select one of the supported languages.
This language selection must be reflected in the provided capabilities document.

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/extended-capabilities)
* [Provide Response Language](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/provide-response-language)
* [Provide Supported Languages](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/provide-supported-languages)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* Let the value of [SupportedLanguage codes](#supported-languages) be ```language-list```.
* For each ```language-list``` as ```lang-code```:
  * Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WFS```, ```REQUEST=GetCapabilities```, ```VERSION=2.0.0``` and ```LANGUAGE=``` + ```lang-code``` to the ```getcapabilities-url```
  * Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes all the tests listed as prerequisites for this test:
    * Check that the [ResponseLanguage code](#response-language) equals the ```lang-code```. If it does not, fail the test for this language.
    * Check that the list of [SupportedLanguage codes](#supported-languages) equals ```language-list```. If not, fail the test for this language.
  * Otherwise fail the test.
* If the test for any of the languages failed, fail the test. Otherwise pass the test.

**Reference(s)**

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirements 55, 56

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
ResponseLanguage code <a name="response-language"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:ResponseLanguage/inspire_common:Language
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:Operation[@name="GetCapabilities"]/ows:DCP/ows:HTTP/ows:Get[1]/@xlink:href
