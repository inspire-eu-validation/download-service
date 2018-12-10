# Language Capabilities Default

**Purpose**: Test that the capabilities document is in default language when resquested with absent language parameter or unsupported language.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without LANGUAGE parameter.

* Send a GetCapabilities with unsupported LANGUAGE parameter.

  * Check if [Title](#title) is the same as the first request.

  * Check if [Abstract](#abstract) is the same as the first request.

* If any of the checks or validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.12
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)
* [INS MDTG](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)

**Test type**: Automated

**Notes**

The multiplicity of [Title](#title) is one.

The multiplicity of [Abstract](#abstract) is one.

Besides 'Title' and 'Abstract' elements, the requirement mention 'Description' and 'Offering Names' fields. But it is not clear where these fields are located in xml structure.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Title <a name="title"></a> | ows:ServiceIdentification/ows:Title |
| Abstract <a name="abstract"></a> | ows:ServiceIdentification/ows:Abstract |