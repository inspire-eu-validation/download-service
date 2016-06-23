# Provide a title element

**Purpose**:

The "title" element of an Atom Download Service feed shall be populated with a human readable title for the feed

**Test method**

* the [feed title](#feedtitle) must be non-empty text; the text content must include at least one alpha-numeric letter.

**Reference(s)**:

* [IR NS](README.md#ref_IR_NS), M1, section 2.2.1, Download Service Metadata parameter
* [TG DL](README.md#ref_TG_DL), Req 5

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed title <a name="feedtitle"></a> | /atom:feed/atom:title
