# Language Capabilities Parameter

**Purpose**: Test that the service accepts the parameter LANGUAGE.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

    * Check if it exists exactly one [Response Language](#responseLanguage) node.

    * Check if it exists exactly one [Supported Languages](#supportedLanguages) node.

    * Check if it exists exactly one [Default Language](#defaultLanguage) node.

* Send a GetCapabilities request with parameter LANGUAGE and value [Default Language](#defaultLanguage).

    * Check if the service accepts the LANGUAGE parameter and the [Response Language](#responseLanguage) is the same as the requested one.

* If any of the checks or validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.11
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Response Language <a name="responseLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language |
| Default Language <a name="defaultLanguage"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |