# Download Service feed links dataset metadata records

**Purpose**: For each [entry](#entry), the Download Service feed must provide a [link to a Dataset metadata record](#datasetdescribedbylink). This link shall have a "rel" attribute with a value of "describedby" and a "type" attribute with a value "application/xml". The link must point to a Dataset metadata record, to which the Service metadata record refers (contains a link to). There must be exactly one link for each [entry](#entry).

**Prerequisites**

**Test method**

For each [entry](#entry):

* the [link to a Dataset metadata record](#datasetdescribedbylink) must be a valid HTTP URI
* there must be only one [link to a Dataset metadata record](#datasetdescribedbylink)
* retrieve the resource at the URI in the [link to a Dataset metadata record](#datasetdescribedbylink) to get the Dataset metadata record (a document with a gmd:MD_Metadata root element)

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 14

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
link to a Dataset metadata record <a name="datasetdescribedbylink"></a> | //atom:entry/atom:link[@rel='describedby' and @type='application/xml']/@href
