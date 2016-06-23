# Download Service feed contains feed updated element

**Purpose**:

The Download Service feed must provide information about the date, time and timezone at which the feed was last updated in the [updated element](#updatedelement).

 **Test method**

* check if the [updated element](#updatedelement) provides a [valid date](#validdate)
* the date must not be in the future or before the year 2012

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 11
* [IR NS](README.md#ref_IR_NS), M1, section 2.2.1, Download Service Metadata parameter

**Test type**: Automated

**Notes**

[1] Not really practical to check if it is actually the correct date of last updating especially as ATOM spec allows this to be for "significant" updates.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
updated element <a name="updatedelement"></a> | /atom:feed/atom:updated
valid date <a name="validdate"></a> | year-from-dateTime(xs:dateTime(/atom:feed/atom:updated))
