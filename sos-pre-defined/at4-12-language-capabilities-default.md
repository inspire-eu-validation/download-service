# Language Capabilities Default

**Purpose**: Check that the capabilities document is in default language when resquested with absent language parameter or unsupported language.

**Prerequisites**

**Test method**

* Send a GetCapabilities request with parameter LANGUAGE and value [Default Language](#defaultLanguage)
* Send a GetCapabilities request without LANGUAGE parameter
  * Check that Description is the same as the first request
  * Check that [Title](#title) is the same as the first request
  * Check that [Abstract](#abstract) is the same as the first request
  * Check that Offering Names is the same as the first request
* Send a GetCapabilities with unsupported LANGUAGE parameter
  * Check that Description is the same as the first request
  * Check that [Title](#title) is the same as the first request
  * Check that [Abstract](#abstract) is the same as the first request
  * Check that Offering Names is the same as the first request
* If any of the checks or validations fails, the test fails

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.12
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Default Language <a name="defaultLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Title <a name="title"></a> | /ows:ServiceIdentification/ows:Title |
| Abstract <a name="abstract"></a> | ows:ServiceIdentification/ows:Abstract |