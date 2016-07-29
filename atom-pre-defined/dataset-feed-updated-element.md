# Dataset feed updated element

**Purpose**: The dataset feed must provide information about the date, time and timezone at which the feed was last updated in the [updated element](#updatedelement).

**Prerequisites**

**Test method**

* check if the [updated element](#updatedelement) provides a [valid date](#validdate).
* the date must not be in the future or before the year 2012

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 24

**Test type**: Automated

**Notes**

Not really practical to check if it is actually the correct date of last updating especially as ATOM spec allows this to be for "significant" updates.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
updated element <a name="updatedelement"></a> | /atom:feed/atom:updated
valid date <a name="validdate"></a> | year-from-dateTime(xs:dateTime(/atom:feed/atom:updated))
