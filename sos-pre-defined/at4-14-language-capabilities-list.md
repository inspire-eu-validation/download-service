# Language Capabilities List

**Purpose**: Test that the supported languages, including the default language, appears in the extended capabilities section of the capabilities document.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

    * Check if it exists exactly one [Supported Languages](#supportedLanguages) node.

    * Check if it exists exactly one [Default Language](#defaultLanguage) node.

    * Check if it exists zero or more [Supported Language](#supportedLanguage) node.

* If any of the checks or validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.14
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**

The multiplicity of [Supported Languages](#supportedLanguages) is 1.

The multiplicity of [Default Language](#defaultLanguage) is 1.

The multiplicity of [Supported Language](#supportedLanguage) is 0 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Response Language <a name="responseLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language |
| Supported Languages <a name="supportedLanguages"></a> | /ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages |
| Default Language <a name="defaultLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Supported Language <a name="supportedLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language |