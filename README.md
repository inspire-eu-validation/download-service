ats-download-atom
=================

Abstract Test Suite for Atom Implementation of Pre-defined Dataset Download Service of INSPIRE Download Services Technical Guidance

*Note*: This ATS is in ready-for-review stage, none of the tests have an official INSPIRE MIG approval.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
TG DL <a name="ref_TG_DL"></a>   | [INSPIRE Download Services Technical Guidance version 3.1](http://inspire.ec.europa.eu/documents/Network_Services/Technical_Guidance_Download_Services_v3.1.pdf)
IR NS <a name="ref_IR_NS"></a>   | [COMMISSION REGULATION (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02009R0976-20101228&from=EN)
IR MD <a name="ref_IR_MD"></a>   | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
ATOM <a name"ref_atom"></a>      | [The Atom Syndication Format](http://tools.ietf.org/html/rfc4287) (RFC 4287)
GeoRSS Simple <a name="ref_georss_simple"></a> | [GeoRSS Simple](http://www.georss.org/simple.html)
OpenSearch <a name="ref_opensearch"></a> | [OpenSearch 1.1 specification, version Draft 5](http://www.opensearch.org/Specifications/OpenSearch/1.1)

## TG Requirement coverage

Based on requirement numbering in [TG DL](#ref_TG_DL).

| Req#  | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ----- | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1     | Datasets as individual entries       | [A.01.TGR1.separatedatasets](a-01-tgr1-separatedatasets.md) | n/a |
| 2     | Atom specification conformance       | [A.02.TGR2.conformtoAtomSpecification](a-02-tgr2-conformtoatomspecification.md) | n/a |
| 3     | GeoRSS Simple conformance            | [A.03.TGR3.conformtoGeoRSS-Simple](a.03.tgr3.conformtogeorss-simple.md) | n/a |
| 4     | OpenSearch conformance               | [A.04.TGR4.conformtoOpenSearch1.1](a-04-tgr4-conformtoopensearch1-1.md) | n/a |
| 5     | Download Service Feed title          | [A.05.IR221.TGR5.feedTitle](a-05-ir221-tgr5-feedtitle.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 6     | Metadata record link for service     | [A.06.IR511.TGR6.linkToMetadataForTheService](a-06-ir511-tgr6-linktometadatafortheservice.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1; [IR MD](#ref_IR_MD), section 2.2.4 |
| 7     | Download Service Feed self reference | [A.07.TGR7.selfreference](a-07-tgr7-selfreference.md) | n/a |
| 8     | OpenSearch Description link          | [A.08.IR222.TGR8.linktoOpenSearchDescription](a-08-ir222-tgr8-linktoopensearchdescription.md) |[IR NS](#ref_IR_NS), M1, section 2.2.2|
| 9     | Download Service Feed ID             | [A.09.TGR9.feedid](a-09-tgr9-feedid.md) | n/a |
| 10    | Download Service Rights     | [A.10.IR221.TGR10.rightselement](a-10-ir221-tgr10-rightselement.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 11    | Download Service Updated    | [A.11.IR221.TGR11.updatedelement](a-11-ir221-tgr11-updatedelement.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 12    | Download Service Author     | [A.12.IR221.TGR12.contactinformation](a-12-ir221-tgr12-contactinformation.md) |[IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 13    | Spatial Data Set identifiers in Service Feed | [A.13.IR221.TGR13.datasetidentifiers](a-13-ir221-tgr13-datasetidentifiers.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 14    | Dataset metadata record links in Service Feed | [A.14.IR221.TGR14.linksToDatasetMetadata](a-14-ir221-tgr14-linkstodatasetmetadata.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 15    | Dataset Feed links in Service Feed   | [A.15.TGR15.linkToDatasetFeed](a-15-tgr15-linktodatasetfeed.md) | n/a |
| 16    | WFS Capabilities document link       | Not testable ||
| 17    | Dataset Feed ID in Service Feed      | [A.16.TGR17.entryHasId](a-16-tgr17-entryhasid.md) |n/a|
| 18    | Dataset Feed title in Service Feed   | [A.17.TGR18.entryTitle](a-17-tgr18-entrytitle.md) |n/a|
| 19    | Dataset Feed Updated element in Service Feed | [A.18.TGR19.entryUpdated](a-18-tgr19-entryupdated.md) |n/a|
| 20    | Dataset CRS category elements in Service Feed | [A.19.IR224.TGR20.entryCRS](a-19-ir224-tgr20-entrycrs.md) | [IR NS](#ref_IR_NS), M1, section 2.2.4|
| 21    | Dataset Feed title in Dataset Feed   | [A.20.IR224.TGR21.datasetFeedTitle](a-20-ir224-tgr21-datasetfeedtitle.md) | [IR NS](#ref_IR_NS), M1, section 2.2.4|
| 22    | Dataset Feed ID in Dataset Feed      | [A.21.TGR22.datasetFeedId](a-21-tgr22-datasetfeedid.md) |n/a|
| 23    | Dataset Feed Rights in Dataset Feed  | [A.22.IR221.TGR23.datasetFeedRights](a-22-ir221-tgr23-datasetfeedrights.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 24    | Dataset Updated in Dataset Feed      | [A.23.IR221.TGR24.datasetFeedUpdated](a-23-ir221-tgr24-datasetfeedupdated.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 25    | Dataset Author in Dataset Feed       | [A.24.IR221.TGR25.datasetFeedContactinformation](a-24-ir221-tgr25-datasetfeedcontactinformation.md) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 26    | Dataset content entry                | [A.25.IR31.TGR26.datasetFeedDownloadLink](a-25-ir31-tgr26-datasetfeeddownloadlink.md) | [IR NS](#ref_IR_NS), M1, section 3.1|
| 27    | Dataset format/CRS specific content entries | [A.26.IR313.TGR27.separateEntriesCRSFormat](a-26-ir313-tgr27-separateentriescrsformat.md) | [IR NS](#ref_IR_NS), M1, section 3.1.3 |
| 28    | Dataset Spatial Object Type link     | [A.27.IR4.TGR28.spatialObjectType](a-27-ir4-tgr28-spatialobjecttype.md) | [IR NS](#ref_IR_NS), M1, section 4|
| 29    | Dataset entry content links          | [A.28.IR31.TGR29.datasetFeedDownloadLinkDetails](a-28-ir31-tgr29-datasetfeeddownloadlinkdetails.md) | [IR NS](#ref_IR_NS), M1, section 3.1 |
| 30    | Dataset entry content media type     | [A.28.IR31.TGR29.datasetFeedDownloadLinkDetails](a-28-ir31-tgr29-datasetfeeddownloadlinkdetails.md) | n/a |
| 31    | Dataset entry content language       | [A.29.IR311.TGR31.languageForDownloadLink](a-29-ir311-tgr31-languagefordownloadlink.md) | [IR NS](#ref_IR_NS), M1, section 3.1.1 |
| 32    | Sectioned dataset entry links        | [A.30.TGR32.downloadMultipleFiles](a-30-tgr32-downloadmultiplefiles.md) |n/a|
| 33    | Sectioned dataset structure          | [A.31.TGR33.downloadMultipleFilesGuidance](a-31-tgr33-downloadmultiplefilesguidance.md) |n/a|
| 34    | Only INSPIRE media types allowed     | [A.32.TGR34.INSPIREmediaTypesOnly](a-32-tgr34-inspiremediatypesonly.md) |n/a|
| 35    | Dataset CRS category elements in Dataset Feed | [A.33.IR224.IR313.TGR35.categoryLabelCRS](a-33-ir224-ir313-tgr35-categorylabelcrs.md) |[IR NS](#ref_IR_NS), M1, section 3.1.3|
| 36    | Alternate languages in Service Feed  | Not testable | n/a |
| 37    | Language request parameter           | Not testable | n/a |
| 38    | Alternate language feed interlinking | Not testable | n/a |
| 39    | OpenSearch Description document      |[A.08.IR222.TGR8.linktoOpenSearchDescription](a-08-ir222-tgr8-linktoopensearchdescription.md), [a.36.tgr41.opensearchgenericsearchqueries.md](a-36-tgr41-opensearchgenericsearchqueries.md), [a.37.ir4.tgr42.opensearchurldescribespatialdataset](a-37-ir4-tgr42-opensearchurldescribespatialdataset.md), [a.38.ir3.tgr43.opensearchurlgetspatialdataset](a-38-ir3-tgr43-opensearchurlgetspatialdataset.md), [a.39.ir3.ir4.tgr44.opensearchqueryexample](a-39-ir3-ir4-tgr44-opensearchqueryexample.md) and [a.40.ir311.ir411.tgr45.opensearchlanguages](a-40-ir311-ir411-tgr45-opensearchlanguages.md) |[IR NS](#ref_IR_NS), M1, section 2.2.2|
| 40    | OpenSearch Description self reference | [A.35.TGR40.openSearchSelfreference](a-35-tgr40-opensearchselfreference.md) |n/a|
| 41    | OpenSearch Generic search results URL template | [A.36.TGR41.openSearchGenericSearchQueries](a-36-tgr41-opensearchgenericsearchqueries.md) |n/a|
| 42    | OpenSearch Describe Spatial Data Set Operation template | [A.37.IR4.TGR42.openSearchUrlDescribeSpatialDataset](a-37-ir4-tgr42-opensearchurldescribespatialdataset.md) | [IR NS](#ref_IR_NS), M1, section 4|
| 43    | OpenSearch Get Spatial Data Set Operation template | [A.38.IR3.TGR43.openSearchUrlGetSpatialDataset](a-38-ir3-tgr43-opensearchurlgetspatialdataset.md) |n/a|
| 44    | OpenSearch Spatial Data Set IDs as example queries | [A.39.IR3.IR4.TGR44.openSearchQueryExample](a-39-ir3-ir4-tgr44-opensearchqueryexample.md) | [IR NS](#ref_IR_NS), M1, section 4|
| 45    | OpenSearch supported languages       | [A.40.IR311.IR411.TGR45.openSearchLanguages](a-40-ir311-ir411-tgr45-opensearchlanguages.md) |[IR NS](#ref_IR_NS), M1, section 4.1.1|

## Tests

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [A.01.TGR1.separatedatasets](a-01-tgr1-separatedatasets.md)       | Ready for review    |
| [A.02.TGR2.conformtoAtomSpecification](a-02-tgr2-conformtoatomspecification.md)  | Ready for review    |
| [A.03.TGR3.conformtoGeoRSS-Simple](a.03.tgr3.conformtogeorss-simple.md)    | Ready for review    |
| [A.04.TGR4.conformtoOpenSearch1.1](a-04-tgr4-conformtoopensearch1-1.md)    | Ready for review    |
| [A.05.IR221.TGR5.feedTitle](a-05-ir221-tgr5-feedtitle.md)         | Ready for review    |
| [A.06.IR511.TGR6.linkToMetadataForTheService](a-06-ir511-tgr6-linktometadatafortheservice.md)  | Ready for review    |
| [A.07.TGR7.selfreference](a-07-tgr7-selfreference.md)             | Ready for review    |
| [A.08.IR222.TGR8.linktoOpenSearchDescription](a-08-ir222-tgr8-linktoopensearchdescription.md)  | Ready for review |
| [A.09.TGR9.feedid](a-09-tgr9-feedid.md)   | Ready for review    |
| [A.10.IR221.TGR10.rightselement](a-10-ir221-tgr10-rightselement.md)   | Ready for review    |
| [A.11.IR221.TGR11.updatedelement](a-11-ir221-tgr11-updatedelement.md) | Ready for review    |
| [A.12.IR221.TGR12.contactinformation](a-12-ir221-tgr12-contactinformation.md) | Ready for review    |
| [A.13.IR221.TGR13.datasetidentifiers](a-13-ir221-tgr13-datasetidentifiers.md) | Ready for review    |
| [A.14.IR221.TGR14.linksToDatasetMetadata](a-14-ir221-tgr14-linkstodatasetmetadata.md) | Ready for review    |
| [A.15.TGR15.linkToDatasetFeed](a-15-tgr15-linktodatasetfeed.md) | Ready for review |
| [A.16.TGR17.entryHasId](a-16-tgr17-entryhasid.md) | Ready for review |
| [A.17.TGR18.entryTitle](a-17-tgr18-entrytitle.md) | Ready for review |
| [A.18.TGR19.entryUpdated](a-18-tgr19-entryupdated.md) | Ready for review |
| [A.19.IR224.TGR20.entryCRS](a-19-ir224-tgr20-entrycrs.md) | Ready for review |
| [A.20.IR224.TGR21.datasetFeedTitle](a-20-ir224-tgr21-datasetfeedtitle.md) | Ready for review |
| [A.21.TGR22.datasetFeedId](a-21-tgr22-datasetfeedid.md) | Ready for review |
| [A.22.IR221.TGR23.datasetFeedRights](a-22-ir221-tgr23-datasetfeedrights.md)  | Ready for review |
| [A.23.IR221.TGR24.datasetFeedUpdated](a-23-ir221-tgr24-datasetfeedupdated.md) | Ready for review |
| [A.24.IR221.TGR25.datasetFeedContactinformation](a-24-ir221-tgr25-datasetfeedcontactinformation.md) | Ready for review |
| [A.25.IR31.TGR26.datasetFeedDownloadLink](a-25-ir31-tgr26-datasetfeeddownloadlink.md) | Ready for review |
| [A.26.IR313.TGR27.separateEntriesCRSFormat](a-26-ir313-tgr27-separateentriescrsformat.md) | Ready for review |
| [A.27.IR4.TGR28.spatialObjectType](a-27-ir4-tgr28-spatialobjecttype.md) | Ready for review |
| [A.28.IR31.TGR29.datasetFeedDownloadLinkDetails](a-28-ir31-tgr29-datasetfeeddownloadlinkdetails.md) | Ready for review |
| [A.29.IR311.TGR31.languageForDownloadLink](a-29-ir311-tgr31-languagefordownloadlink.md) | Ready for review |
| [A.30.TGR32.downloadMultipleFiles](a-30-tgr32-downloadmultiplefiles.md) | Ready for review |
| [A.31.TGR33.downloadMultipleFilesGuidance](a-31-tgr33-downloadmultiplefilesguidance.md) | Ready for review |
| [A.32.TGR34.INSPIREmediaTypesOnly](a-32-tgr34-inspiremediatypesonly.md) | Ready for review |
| [A.33.IR224.IR313.TGR35.categoryLabelCRS](a-33-ir224-ir313-tgr35-categorylabelcrs.md) | Ready for review |
| [A.35.TGR40.openSearchSelfreference](a-35-tgr40-opensearchselfreference.md)  | Ready for review |
| [A.36.TGR41.openSearchGenericSearchQueries](a-36-tgr41-opensearchgenericsearchqueries.md) | Ready for review |
| [A.37.IR4.TGR42.openSearchUrlDescribeSpatialDataset](a-37-ir4-tgr42-opensearchurldescribespatialdataset.md) | Ready for review |
| [A.38.IR3.TGR43.openSearchUrlGetSpatialDataset](a-38-ir3-tgr43-opensearchurlgetspatialdataset.md) | Ready for review |
| [A.39.IR3.IR4.TGR44.openSearchQueryExample](a-39-ir3-ir4-tgr44-opensearchqueryexample.md) | Ready for review |
| [A.40.IR311.IR411.TGR45.openSearchLanguages](a-40-ir311-ir411-tgr45-opensearchlanguages.md) | Ready for review |

## Open issues

* Is it allowed for more than one Download Service Feed to point to the same Dataset Feed? If yes, and if these Download Service Feeds contain different entries pointing to this Dataset Feed, which parent feed should be used for validation? One example for the possible conflict would be different CRS categories in the Download Service Feed entries.

* Should it be allowed for the Dataset Feed to additionally contain download links to files containing the data in other CRSes than the ones mentioned in it's parent Download Service Feed, or should the CRS (category) list in the Download Service Feed entry and the corresponding Dataset Feed match exactly?

* Is the hreflang attribute mandatory in the Dataset Feed link entries event if the data is provided only in a single language? If so, the test [A.29.IR311.TGR31.languageForDownloadLink](a-29-ir311-tgr31-languagefordownloadlink.md) is not automatically testable and the should be removed.

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
atom           | http://www.w3.org/2005/Atom
georss         | http://www.georss.org/georss
gmd            | http://www.isotc211.org/2005/gmd
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
os             | http://a9.com/-/spec/opensearch/1.1/
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
