# Language Capabilities

**Purpose**: Check that the capabilities document might be retrieved in different languages. The supported languages are shown in metadata.

**Prerequisites**

**Test method**

* Send a GetCapabilities request
* Validate that it exists exactly one [Response Language](#responseLanguage) node
* Validate that it exists exactly one [Supported Languages](#supportedLanguages) node
* Validate that it exists exactly one [Default Language](#defaultLanguage) node
* Validate that it exists zero or more [Supported Language](#supportedLanguage) node
* For every supported language, send GetCapabilities request with parameter LANGUAGE. The parameter values are based on ISO 639-2/B alpha 3 codes as used in [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
  * Validate that the [Response Language](#responseLanguage) is the same as the requested one
  * Validate that the natural language fields are in the requested language
  * Validate that the list of supported languages is invariant for each GetCapabilities-Response regardless of the response language
* Send GetCapabilities request with an unsupported language
  * Validate that the response language is the same as the default language
  * Validate that Description, [Title](#title), [Abstract](#abstract) and Offering Names are in the default language
* If any of the checks or validations fails, the test fails


**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.9, 4.10, 4.11, 4.12, 4.13 and 4.14
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