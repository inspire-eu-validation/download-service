# Download Service feed contains feed rights element

**Purpose**:

The Download Service feed must provide information about rights or restrictions for that feed in the feed's [rights element](#rightselement).

 **Test method**

* the [rights element](#rightselement) must be non-empty text; the text content must include at least one alpha-numeric letter.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 10
* [IR NS](README.md#ref_IR_NS), M1, section 2.2.1, Download Service Metadata parameter

**Test type**: Automated

**Notes**

[1] It is only possible to test for existence of an alphanumerical character; testing the contents of the element is not possible to implement without further specification

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
rights element <a name="rightselement"></a> | /atom:feed/atom:rights
