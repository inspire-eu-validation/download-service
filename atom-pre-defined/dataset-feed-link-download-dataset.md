# Dataset feed link download dataset

**Purpose**: Each dataset feed [entry](#entry) must contain an Atom "[link](#downloadlink)" element that links to the pre-defined dataset file described by the [entry](#entry) (e.g. a GML file). The value of the "rel" attribute of this element must be "alternate" and a "length" attribute (providing the length of the linked resource in octets \*) must be provided if possible. Where a dataset is provided in multiple physical files, additional "[link](#downloadlink)" elements must be provided in the feed [entry](#entry), one link for each physical file.

**Prerequisites**

**Test method**

* Test if at least one feed entry is available with at least one [link](#downloadlink) to download a file.
* Retrieve the resource at the URI in the [links](#downloadlink) element and check that fetching them does not result in an error or a zero-length resource. This may be tested using the HTTP HEAD method or alternatively validators using HTTP GET may interrupt the download of the resource after receiving enough of the response to determine the above conditions. Validators must not create any errors considering the file format integrity or completeness. When retrieving the resource, HTTP codes for success are: 200, 204, 301, 302, 303. For 30x responses, the redirection link should be followed.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirements 26, 29

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
link <a name="downloadlink"></a> | //atom:entry/atom:link[(@rel='alternate' and @type!='application/atom+xml' and number(@length) > 0) or (@rel='section')]