# Language request empty and unsupported

**Purpose**: Test that Title and Abstract fields are provided in default language when the AcceptLanguage parameter is not set in the request or when it is set with a wrong value.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without AcceptLanguages parameter.

* Send a GetCapabilities with unsupported AcceptLanguages parameter.

  * Check if [Title](#title) is the same as the first request.

  * Check if [Abstract](#abstract) is the same as the first request.

* Send a GetCapabilities with AcceptLanguages parameter set to default language.

  * Check if [Title](#title) is the same as the first request.

  * Check if [Abstract](#abstract) is the same as the first request.

* If any of the checks or validations fails, the test fails.

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 7

**Test type**: Automated

**Notes**

The multiplicity of [Title](#title) is 1.

The multiplicity of [Abstract](#abstract) is 1.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| Title <a name="title"></a> | ows:ServiceIdentification/ows:Title |
| Abstract <a name="abstract"></a> | ows:ServiceIdentification/ows:Abstract |