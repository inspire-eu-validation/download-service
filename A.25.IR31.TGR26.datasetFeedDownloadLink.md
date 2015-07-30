# Dataset feed contains link to download dataset

**Purpose**:

The dataset feed must provide at least one feed [entry](#entry) with [links to download](#downloadlink) the pre-defined dataset (e.g. as a GML file).

 **Test method**

* test if at least one feed entry is available with at least one [link to download](#downloadlink) a file
* resolve all [links to download](#downloadlink) in the dataset feed.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 26
* [IR NS](README.md#ref_IR_NS), M1, section 3.1, Get Spatial Data Set request

**Test type**:

Automated

**Notes**

[1] when resolving the links, HTTP codes for success are: 200,301,302,303
[2] it is up to the implementing tool to decide to use HTTP GET or HTTP HEAD.


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
link to download <a name="downloadlink"></a> | //atom:entry/atom:link[(@rel='alternate' and @type!='application/atom+xml' and number(@length) > 0) or (@rel='section')]
