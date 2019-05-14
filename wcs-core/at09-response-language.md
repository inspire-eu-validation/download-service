# Response language

**Purpose**: Test that the response language changes according with the AcceptLanguages parameter of the GetCapabilities request.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without AcceptLanguages parameter.

  * Check if the [Response Language](#responseLanguage) is the same as the [Default Language](#defaultLanguage).

* Send a GetCapabilities request with an invalid value in the AcceptLanguages parameter.

  * Check if the [Response Language](#responseLanguage) is the same as the [Default Language](#defaultLanguage).

* For every [Supported Language](#supportedLanguage), send a GetCapabilities request with the parameter AcceptLanguages equal to that language

  * Check if the [Response Language](#responseLanguage) is the same as the requested one.

* If any of the checks or validations fails, the test fails.

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 9

**Test type**: Automated

**Notes**

The multiplicity of [Response Language](#responseLanguage) is 1.

The multiplicity of [Default Language](#defaultLanguage) is 1.

The multiplicity of [Supported Language](#supportedLanguage) is 0 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| Response Language <a name="responseLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language |
| Default Language <a name="defaultLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Supported Language <a name="supportedLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language |
