# Separate entries for each format/CRS combination

**Purpose**:

The Dataset Feed must contain separate [entries](#entry) for each format/CRS combination in which the pre-defined dataset is available to download.

 **Test method**

* Test that no entries exist with the [same alternate link and type (format)](#samealternatelink) in that entry.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 27
* [IR NS](README.md#ref_IR_NS), M1, section 3.1.3, Get Spatial Data Set Operation / Coordinate Reference System parameter

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
same alternate link and type <a name="samealternatelink"></a> | //atom:entry[./atom:link[@rel='alternate' and @type!=../atom:link[1][@rel='alternate']/@type]]
