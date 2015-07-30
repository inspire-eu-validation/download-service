# OpenSearch Description provides URL for generic search queries

**Purpose**:

The OpenSearch description must contain a ["Url" element](#urlelement) that describes a template URL for generic search queries. The value of the "rel" attribute of this element must be "results", the value of the "type" attribute must be "text/html".

**Test method**

* test if the OpenSearch Description provides a [generic search queries url](#genericsearchurl)
* resolve the [generic search queries url](#genericsearchurl) and test if it provides a document with content-type "text/html"

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 41
* [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Test type**:

Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
url element <a name="urlelement"></a> | /os:OpenSearchDescription/os:Url
generic search queries url <a name="genericsearchurl"></a> | /os:OpenSearchDescription/os:Url[@rel='results' and @type='text/html']/@template
