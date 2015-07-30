# Download Service feed provides CRS information for each entry

**Purpose**:

Each feed entry must contain an Atom "category" element for each CRS in which the pre-defined dataset is available. This category element must refer to a well-known definition of a coordinate reference system.

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if at least one valid [category element](#category) is provided.

**Reference(s)**:

* [IR NS](README.md#ref_IR_NS), M1, section 2.2.4, Spatial Data Sets Metadata parameters
* [TG DL](README.md#ref_TG_DL), Req 20

**Test type**:

Automated

**Notes**
Testing the contents of the value for being “well known” is hard to automate / determine unambigiously. So only check on existence of the required element.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
category element <a name="category"></a> | //atom:entry/atom:category[string-length(@term)>0 and string-length(@label)>0]
