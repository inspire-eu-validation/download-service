# Download Service feed contains links to dataset metadata records

**Purpose**:

For each [entry](#entry), the Download Service feed must provide a [link to a Dataset metadata record](#datasetdescribedbylink). This link shall have a "rel" attribute with a value of "describedby" and a "type" attribute with a value "application/xml". The link must point to a Dataset metadata record, to which the Service metadata record refers (contains a link to). There must be exactly one link for each [entry](#entry).

**Test method**

* Resolve the [describedby link](#describedbylink) to get the metadata document of the service

For each [entry](#entry):

* the [link to a Dataset metadata record](#datasetdescribedbylink) must be a valid HTTP URI
* there must be only one [link to a Dataset metadata record](#datasetdescribedbylink)
* resolve the [link to a Dataset metadata record](#datasetdescribedbylink) to get the Dataset metadata record

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 14
* [IR NS](README.md#ref_IR_NS), section 2.2.1, Discovery Service Metadata parameters

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
describedby link <a name="describedbylink"></a> | /atom:feed/atom:link[@rel='describedby' and (@type='application/xml' or @type='application/vnd.ogc.csw.GetRecordByIdResponse_xml')]/@href
entry <a name="entry"></a> | //atom:entry
link to a Dataset metadata record <a name="datasetdescribedbylink"></a> | //atom:entry/atom:link[@rel='describedby' and @type='application/xml']/@href
dataset identifier <a name="datasetidentifier"></a> | gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:identifier
