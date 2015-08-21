# Dataset feed contains link to download dataset

**Purpose**:

Each feed [entry](#entry) must contain an Atom "[link](#downloadlink)" element that links to the pre-defined dataset file described by the [entry](#entry). The value of the "rel" attribute of this element must be "alternate" and a "length" attribute (providing the length of the linked resource in octets \*) must be provided if possible. Where a dataset is provided in multiple physical files, additional "[link](#downloadlink)" elements must be provided in the feed [entry](#entry), one link for each physical file.

\* 1 octet = 8 bits (usually synonymous with 1 byte)

**Test method**

* Test if at least one feed entry is available with at least one [link](#downloadlink) to download a file.
* Resolve all [links](#downloadlink) in the dataset feed and check that fetching them does not result in an error or a zero-length resource. Validators may interrupt the downloads of the resources after receiving enough of the response to determine the above conditions. Validators must not create any errors considering the file format integrity or completeness.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 29
* [IR NS](README.md#ref_IR_NS), M1, section 3.1, Get Spatial Data Set request

**Test type**:

Automated

**Notes**

[1] this overlaps with TG Requirement 26. This requirement gives more details about how to encode the link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
link <a name="downloadlink"></a> | //atom:entry/atom:link[(@rel='alternate' and @type!='application/atom+xml' and number(@length) > 0) or (@rel='section')]
