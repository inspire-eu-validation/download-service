# Each entry has CRS information

**Purpose**:

Each CRS representation must have a [category element](#category) which refers to the CRS definition and code.

**Test method**

* For each [entry](#entry) in the Dataset feed, check if one valid [category element](#category) is provided for the CRS.

**Reference(s)**:

* [IR NS](README.md#ref_IR_NS), M1, section 2.2.4, Spatial Data Sets Metadata parameters
* [IR NS](README.md#ref_IR_NS), M1, section 3.1.3, Coordinate Reference System parameter
* [TG DL](README.md#ref_TG_DL), Req 35

**Test type**:

Automated

**Notes**

Testing the contents of the value for being a valid CRS code is hard to automate / determine unambigiously. So only check on existence of the required element.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
category element <a name="category"></a> | //atom:entry/atom:category[string-length(@term)>0 and string-length(@label)>0]
