# Provide guidance for downloading multiple physical files

**Purpose**: Where a dataset is provided in multiple physical files: a description of the dataset structure must be provided EITHER in an atom "[content](#contentelement)" element as free text, OR in an external document which is the target of another "[link](#alternatelink)" element. Where a "[link](#alternatelink)" element is used this element shall have a "rel" value equal to "alternate" and a suitable media type shall be used for the "type" value.

**Prerequisites**

**Test method**

* If [links with a rel attribute of "section"](#sectionlink) are provided, then there must be either an [alternate link](#alternatelink) or an Atom [content](#contentelement) element. See Note [1] as well.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 33

**Test type**:

Automated

**Notes**

[1] The test can also be interpreted as: entries with a section link, but without an alternate link and without an Atom content element must not exist in the feed. The appropriate XPath-test for this is: empty(//atom:entry[./atom:link[@rel='section'] and count(./atom:link[@rel='alternate'])=0 and count(./atom:content) = 0])

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
section link <a name="sectionlink"></a> | //atom:entry/atom:link[@rel='section']
(alternate) link <a name="alternatelink"></a> | //atom:entry/atom:link[@rel='section']
content element <a name="contentelement"></a>| //atom:entry[count(./atom:link[@rel='section'])
