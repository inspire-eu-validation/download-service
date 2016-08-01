# Download service feed: Provide link to metadata record for the download service

**Purpose**: The Download Service feed must provide a link to a metadata record, that describes the Download Service. The link must be at the feed-level and have a "rel" attribute of "describedby" and "type" attribute of "application/xml" or "application/vnd.ogc.csw.GetRecordByIdResponse_xml".

**Prerequisites**

**Test method**

* check existence of the [describedby link](#describedbylink) that refers to the metadata document
* retrieve the resource at the URI in the [describedby link](#describedbylink) using HTTP GET to get the metadata document of the service
* the metadata document must be a valid XML document
* the metadata document must have a [gmd:MD_Metadata element](#md_metadata_element) as the root element
* the metadata document must have a [Resource Locator](#resourcelocator)
* retrieve the resource at the URI in the [Resource Locator](#resourcelocator) element, which must be an Atom Download Service Feed document
* this Atom Download Service Feed document (refered from the metadata document) must contain a [describedby link](#describedbylink) that is the same as the [describedby link](#describedbylink) of the first step

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 6


**Test type**: Automated

**Notes**

* The INSPIRE language request parameters in the Resource Locator to the Atom Download Service Feed URLs must be ignored in the comparison of the last step of the test method

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
describedby link <a name="describedbylink"></a> | /atom:feed/atom:link[@rel='describedby' and (@type='application/xml' or @type='application/vnd.ogc.csw.GetRecordByIdResponse_xml')]/@href
gmd:MD_Metadata element <a name="md_metadata_element"></a> | /gmd:MD_Metadata
Resource Locator <a name="resourcelocator"></a>| //gmd:distributionInfo/\*/gmd:transferOptions/\*/gmd:onLine/\*/gmd:linkage
