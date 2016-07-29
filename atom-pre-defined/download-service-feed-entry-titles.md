# Download Service feed: entry titles

**Purpose**: The title element of an entry must be populated with a human readable title for that entry.

**Prerequisites**

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if an [entry title](#entrytitle) is provided.
* The [entry title](#entrytitle) must be non-empty text; the text content must include at least one alpha-numeric letter.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 18

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
entry title <a name="entrytitle"></a> | //atom:entry/atom:title
