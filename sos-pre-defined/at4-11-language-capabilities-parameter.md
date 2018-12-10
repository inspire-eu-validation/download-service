# Language Capabilities Parameter

**Purpose**: Test that the service accepts the parameter LANGUAGE.

**Prerequisites**

**Test method**

* Send a GetCapabilities request with parameter LANGUAGE and value [Default Language](#defaultLanguage).

    * Check if the service accepts the LANGUAGE parameter and the [Response Language](#responseLanguage) is the same as the requested one.

    * Check if [Default Language](#defaultLanguage) is a valid ISO 639-2/B alpha 3 code.

    * For each [Supported Language](#supportedLanguage):

        * Check if [Supported Language](#supportedLanguage) is a valid ISO 639-2/B alpha 3 code.

* If any of the checks or validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.11
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**

The multiplicity of [Response Language](#responseLanguage) is 1.

The multiplicity of [Default Language](#defaultLanguage) is 1.

The multiplicity of [Supported Language](#supportedLanguage) is 0 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Response Language <a name="responseLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language |
| Default Language <a name="defaultLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Supported Language <a name="supportedLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language |