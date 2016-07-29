# Multiple links for multiple physical files

**Purpose**: Where a dataset is provided in multiple physical files: each file must be linked to via a separate [link](#downloadlink) element. Each of these [link](#downloadlink) elements shall have a "rel" value equal to "section".

**Prerequisites**

**Test method**

* If links with a rel attribute of "section" are provided, then there must be multiple [links](#downloadlink). So the [number of section links](#nrsectionlinks) must not be exactly 1.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 32

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link <a name="downloadlink"></a> | //atom:entry/atom:link[@rel='section']
number of section links <a name="nrsectionlinks"></a>| //atom:entry[count(./atom:link[@rel='section'])
