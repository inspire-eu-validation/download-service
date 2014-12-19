# Conform to the OpenSearch specification

**Purpose**: 

The referenced OpenSearch Description must conform to the OpenSearch 1.1 specification 

**Test method**

* resolve the [link to the OpenSearch Description](#opensearchlink) to get the OpenSearch Description
* validate the OpenSearch Description to [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Reference(s)**: 

* TG, Req 4
* [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Test type**: Automated

**Notes**

There is no official XML schema however. So the ETS needs to implement the test based on the schema document directly.


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to the OpenSearch Description <a name="opensearchlink"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@href