# Separate entries for each format/CRS combination

**Purpose**:

The Dataset Feed must contain separate [entries](#entry) for each format/CRS combination in which the pre-defined dataset is made available for download.

 **Test method**

* For all [alternative link types](#alternatelinktypes) for this Dataset Feed, check that there are no duplicate values.
* Find and retrieve the all the Download Service Feed documents containing an entry pointing to this Dataset Feed (see note 1). For each of the entries found this way:
  * For each [category element](#category) in these entries, check that at least one entry exists in the Dataset Feed containing the a category element with an identical term attribute.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 27
* [IR NS](README.md#ref_IR_NS), M1, section 3.1.3, Get Spatial Data Set Operation / Coordinate Reference System parameter

**Test type**:

Automated

**Notes**

1. The method of discovering the parent Download Service Document(s) is left to be solved by the validator implementation. If the Dataset Feed contain the [up-link](#uplink) element it must be used for the parent feed discovery. If no [up-link](#uplink) exists, the validator should use the information about the parent-child relation previously collected when validating the Download Service Feeds pointing to the Dataset Feed. If the validator has not (yet) followed any Download Service Feed entry links to validate this Dataset Feed, it should postpone validation until the parent feed is discovered.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
alternate link types <a name="alternatelinkentries"></a> | //atom:entry[./atom:link[@rel='alternate']]/atom:link/@type
category element <a name="category"></a> | //atom:entry/atom:category[string-length(@term)>0 and string-length(@label)>0]
term attribute <a name="term"></a> | ./atom:category[string-length(@term)>0 and string-length(@label)>0]/@term
up-link <a name="uplink"></a> | /atom:link[@rel='up' and @type='application/atom+xml']
