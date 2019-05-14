# Natural language fields

**Purpose**: Test that the natural language fields are in the requested language.

**Prerequisites**

**Test method**

* Send a GetCapabilities request to the service endpoint with a supported language as parameter. Into the response:

	* Check manually that the Titles and Abstracts fields are in the requested language.

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 3

**Test type**: Manual

**Notes**

The AcceptLanguages parameter might be obtained from [SupportedLanguages](#SupportedLanguages).

Example of languaged request:

http://<i></i>myserver<i></i>.ac.uk/some/folders/ows?service=WCS&request=GetCapabilities&AcceptVersions=2.0.1,2.0.0&AcceptLanguages=en&

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| Supported Languages <a name="supportedLanguages"></a> | inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages |
