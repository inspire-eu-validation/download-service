# OpenSearch Description provides languages

**Purpose**: 
For each language supported by the download service, the OpenSearch description must contain a ["Language" element](#languageelement) that contains the language code. The first ["Language" element](#languageelement) must contain the Default Language.

**Test method**

* test if there is at least one ["Language" element](#languageelement)

**Reference(s)**: 

* IR section 3 (3.1-3.2.1), 4 (4.1-4.2.1)
* TG, Req 45
* [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Test type**: 

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Language element <a name="languageelement"></a> | /os:OpenSearchDescription/os:Language