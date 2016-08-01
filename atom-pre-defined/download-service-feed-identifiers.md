# Download Service feed identifiers

**Purpose**: Each feed [entry](#entry) in a Download Service Feed must provide an [identifier](#identifier) for that entry. This identifier must be an HTTP URI.

**Prerequisites**

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if exactly one [identifier](#identifier) is provided.
* For each [identifier](#identifier) check that it begins with "http".

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 17

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
identifier <a name="identifier"></a> | //atom:entry/atom:id
