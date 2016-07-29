# Download service feed: Provide a title element

**Purpose**: The "title" element of an Atom Download Service feed shall be populated with a human readable title for the feed

**Prerequisites**

**Test method**

* The [feed title](#feedtitle) must be non-empty text; the text content must include at least one alpha-numeric character.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 5

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed title <a name="feedtitle"></a> | /atom:feed/atom:title
