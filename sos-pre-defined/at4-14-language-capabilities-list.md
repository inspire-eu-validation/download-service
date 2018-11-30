# Language Capabilities List

**Purpose**: Check that the supported languages, including the default language, appears in the extended capabilities section of the capabilities document.

**Prerequisites**

**Test method**

* Send a GetCapabilities request
* Validate that it exists exactly one [Supported Languages](#supportedLanguages) node
* Validate that it exists exactly one [Default Language](#defaultLanguage) node
* Validate that it exists zero or more [Supported Language](#supportedLanguage) node
* For every supported language, send GetCapabilities request with parameter LANGUAGE
  * Validate that the list of supported languages is invariant for each GetCapabilities-Response regardless of the response language
* If any of the checks or validations fails, the test fails


**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.14
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Response Language <a name="responseLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language |
| Supported Languages <a name="supportedLanguages"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages |
| Default Language <a name="defaultLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Supported Language <a name="supportedLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language |
| Title <a name="title"></a> | /ows:ServiceIdentification/ows:Title |
| Abstract <a name="abstract"></a> | ows:ServiceIdentification/ows:Abstract |