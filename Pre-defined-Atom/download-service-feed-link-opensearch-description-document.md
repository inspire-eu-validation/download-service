# Download Service feed link OpenSearch Description document

**Purpose**:

The Download Service feed must provide a [link to an OpenSearch Description document](#opensearchlink), that provides the operations metadata for the Download Service. The value of the 'rel' attribute of this link element must be 'search', the [hreflang attribute](#hreflang) must use the appropriate language code and the 'type' attribute must be 'application/opensearchdescription+xml'.

 **Test method**

* check existence of the [link to an OpenSearch Description document](#opensearchlink)
* the [link to an OpenSearch Description document](#opensearchlink) must resolve to a OpenSearch Description Document


**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 8
* [OpenSearch](README.md#ref_opensearch)

**Test type**: Automated

**Notes**

[1] Test on validity of the OpenSearch Description Document is covered in [Conform to the OpenSearch specification.md](conform-to-the-opensearch-specification.md)

The [hreflang attribute](#hreflang) that is referred to in the TG seems to be unnecessary. The MIWP-5 workgroup recommends the TG editors to remove the part regarding the [hreflang attribute](#hreflang) from requirement 8.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to OpenSearch description <a name="opensearchlink"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@href
hreflang attribute <a name="hreflang"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@hreflang
