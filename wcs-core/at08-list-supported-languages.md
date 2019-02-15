# List of supported languages

**Purpose**: Test that the service provides a list of supported languages.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

    * Check that it exists exactly one [Supported Languages](#supportedLanguages) node.

    * Check that it exists exactly one [Default Language](#defaultLanguage) node.

    * Check that it exists zero or more [Supported Language](#supportedLanguage) node.
	
	* Check that all languages provided are valid EU language ISO 639-2/B code: bul, cze, dan, dut, eng, pol, est, fin, fre, ger, gre, hun, gle, hrv, ita, lav, ger, lit, mlt, nor, por, rum, roh, slo, slv, spa, swe or ice.

* If any of the checks or validations fails, the test fails.

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 8

**Test type**: Automated

**Notes**

The multiplicity of [Supported Languages](#supportedLanguages) is 1.

The multiplicity of [Default Language](#defaultLanguage) is 1.

The multiplicity of [Supported Language](#supportedLanguage) is 0 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities/ows:ExtendedCapabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| Supported Languages <a name="supportedLanguages"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages |
| Default Language <a name="defaultLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language |
| Supported Language <a name="supportedLanguage"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language |