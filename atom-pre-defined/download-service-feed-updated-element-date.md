# Download Service feed updated element date

**Purpose**: The updated element of an entry must be populated with a date, time and timezone at which the feed entry was last updated..

**Prerequisites**

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if the [updated](#updated) element provides a [valid date](#validdate).
* A date must not be in the future or before the year 2012.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 19

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
updated element <a name="updated"></a> | //atom:entry/atom:updated
valid date <a name="validdate"></a> | year-from-dateTime(xs:dateTime(atom:updated))
