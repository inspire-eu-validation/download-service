# Provide link to metadata record for Download Service

**Purpose**:

The Download Service feed must provide a link to a metadata record, that describes the Download Service. The link must be at the feed-level and have a "rel" attribute of "describedby" and "type" attribute of "application/xml" or "application/vnd.ogc.csw.GetRecordByIdResponse_xml".

**Test method**

* check existence of the [describedby link](#describedbylink) that refers to the metadata document
* resolve the [describedby link](#describedbylink) to get the metadata document of the service
* the metadata document must be a valid XML document
* the metadata document must have a [gmd:MD_Metadata element](#md_metadata_element) as the root element
* the metadata document must have a [Resource Locator](#resourcelocator)
* the [Resource Locator](#resourcelocator) must resolve to an Atom Download Service Feed document
* this Atom Download Service Feed document (refered from the metadata document) must contain a [describedby link](#describedbylink) that is the same as the [describedby link](#describedbylink) of the first step

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 6


**Test type**: Automated

**Notes**

[1] the INSPIRE language request parameters in the Resource Locator to the Atom Download Service Feed URLs must be ignored in the comparison of the last step of the test method

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
describedby link <a name="describedbylink"></a> | /atom:feed/atom:link[@rel='describedby' and (@type='application/xml' or @type='application/vnd.ogc.csw.GetRecordByIdResponse_xml')]/@href
gmd:MD_Metadata element <a name="md_metadata_element"></a> | /gmd:MD_Metadata
Resource Locator <a name="resourcelocator"></a>| //gmd:distributionInfo/\*/gmd:transferOptions/\*/gmd:onLine/\*/gmd:linkage
