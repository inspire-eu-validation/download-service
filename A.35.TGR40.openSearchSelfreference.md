# OpenSearch Description provides URI to itself

**Purpose**:

The OpenSearch description must contain a ["Url" element](#urlelement) that describes an HTTP URI for the OpenSearch Description document. The value of the "rel" attribute of this element must be "self", the value of the "type" attribute must be "application/opensearchdescription+xml" and the value of the "template" attribute must be the HTTP URI of the document.

**Test method**

* test if the OpenSearch Description provides a [self "Url"](#selfurl)
* test if the value of the [self "Url"](#selfurl) is the same as the URI of the OpenSearch Description that is being tested

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 40
* [OpenSearch](README.md#ref_opensearch)

**Test type**:

Automated

**Notes**

[1] The URI of the OpenSearch Description must be provided in the Download Service. See TG Requirement 8 for details.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
url element <a name="urlelement"></a> | /os:OpenSearchDescription/os:Url
self url <a name="selfurl"></a> | /os:OpenSearchDescription/os:Url[@rel='self' and @type='application/opensearchdescription+xml']/@template
