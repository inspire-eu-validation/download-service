# Dataset Feed: provide a title element

**Purpose**: 

The "title" element of an Atom Dataset feed must be populated with a human readable title for the feed

**Test method**

* the [feed title](#feedtitle) must be non-empty text; the text content must include at least one alpha-numeric letter.

**Reference(s)**: 

* IR section 2.2.4, Spatial Data Sets Metadata parameters
* TG, Req 21

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed title <a name="feedtitle"></a> | /atom:feed/atom:title