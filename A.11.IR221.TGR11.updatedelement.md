# Download Service feed contains feed updated element

**Purpose**:

The Download Service feed must provide information about the date, time and timezone at which the feed was last updated in the [updated element](#updatedelement).

 **Test method**

* check if the [updated element](#updatedelement) exists and contains a correctly formatted date, including time and timezone.
* the date must not be in the future or too far in the past

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 11
* [IR NS](README.md#ref_IR_NS), M1, section 2.2.1, Download Service Metadata parameter

**Test type**: Automated

**Notes**

[1] Not really practical to check if it is actually the correct date of last updating especially as ATOM spec allows this to be for "significant" updates.
[2] What should we consider too far in the past? Before 2000?

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
updated element <a name="updatedelement"></a> | /atom:feed/atom:updated
