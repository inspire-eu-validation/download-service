# Download Service feed provides identifiers for each entry

**Purpose**: 

Each feed [entry](#entry) in a Download Service Feed must provide an [identifier](#identifier) for that entry. This identifier must be an HTTP URI.

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if exactly one [identifier](#identifier) is provided.
* For each [identifier](#identifier) check that it begins with "http".

**Reference(s)**: 

* TG, Req 17

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
identifier <a name="identifier"></a> | //atom:entry/atom:id