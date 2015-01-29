# Download Service feed provides an updated element for each entry

**Purpose**: 

The updated element of an entry must be populated with a date, time and timezone at which the feed entry was last updated..

**Test method**

* For each [entry](#entry) in the Download Service Feed, check if the [updated](#updated) element provides a [valid date](#validdate).

**Reference(s)**: 

* TG, Req 19

**Test type**: 

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
updated element <a name="updated"></a> | //atom:entry/atom:updated
valid date <a name="validdate"></a> | year-from-dateTime(xs:dateTime(atom:updated))
