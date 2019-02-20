# Protocol bindings

**Purpose**: Test that the service supports at least one of the WCS protocol bindings KVP, POST or XML/SOAP.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

    * Check that at least one [Profile](#profile) element contains one of the following values:

        * http://<i></i>www<i></i>.opengis.net/spec/WCS_protocol-binding_post-xml/1.0

        * http://<i></i>vwww<i></i>.opengis.net/spec/WCS_protocol-binding_soap/1.0

        * http://<i></i>www<i></i>.opengis.net/spec/WCS_protocol-binding_get-kvp/1.0.1

**Reference(s)**

* [INS TG WCS](https://inspire.ec.europa.eu/id/document/tg/download-wcs), Requirement 2
* [OGC 06-121r9, OGC Web Service Common Specification, version 2.0](https://www.opengeospatial.org/standards/common), HTTP GET, KVP encoding, HTTP POST and SOAP encoding

**Test type**: Automated

**Notes**

The multiplicity of [Profile](#profile) is 1 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /wcs:Capabilities) |
| --------------------------------------------------- | -------------------------------------------------------------- |
| Profile <a name="profile"></a> | ows:ServiceIdentification/ows:Profile |