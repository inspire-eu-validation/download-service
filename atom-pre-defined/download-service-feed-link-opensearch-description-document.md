# Download Service feed: link OpenSearch Description document

**Purpose**: The Download Service feed must provide a [link to an OpenSearch Description document](#opensearchlink), that provides the operations metadata for the Download Service. The value of the 'rel' attribute of this link element must be 'search', the [hreflang attribute](#hreflang) must use the appropriate language code and the 'type' attribute must be 'application/opensearchdescription+xml'.

**Prerequisites**

**Test method**

* check existence of the [link](#opensearchlink) to OpenSearch description
* the [link](#opensearchlink) must retrieve an OpenSearch Description Document (root element "OpenSearchDescription" in namespace "http://a9.com/-/spec/opensearch/1.1/")

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirements 8, 39
* [OpenSearch](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_opensearch)

**Test type**: Automated

**Notes**

As discussed in the [overview](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#dep) the OpenSearch description must conform to the OpenSearch specification. 

The [hreflang attribute](#hreflang) that is referred to in the TG seems to be unnecessary. The MIWP-5 workgroup recommends the TG editors to remove the part regarding the [hreflang attribute](#hreflang) from requirement 8.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link <a name="opensearchlink"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@href
hreflang attribute <a name="hreflang"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@hreflang
