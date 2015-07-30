ats-download-atom
=================

Abstract Test Suite for Atom Implementation of Pre-defined Dataset Download Service of INSPIRE Download Services Technical Guidance

*Note*: This ATS is in draft stage, none of the tests have an official INSPIRE MIG approval.

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
OpenSearch <a name="ref_opensearch"></a> | [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

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

## TG Requirement coverage

Based on requirement numbering in [TG DL](#ref_TG_DL).

TODO

## Tests

This Conformance Class contains the following tests:

| Identifier                                                        | Origin | Mechanical | Status   |
| ----------------------------------------------------------------- | ------ | ---------- | -------- |
| [A.01.TGR1.separatedatasets](A.01.TGR1.separatedatasets.md)    | TG     | Yes        | Ready for review    |
| [A.02.TGR2.conformtoAtomSpecification](A.02.TGR2.conformtoAtomSpecification.md)    | TG     | Yes        | Ready for review    |
| [A.03.TGR3.conformtoGeoRSS-Simple](A.03.TGR3.conformtoGeoRSS-Simple.md)    | TG     | Yes        | Ready for review    |
| [A.04.TGR4.conformtoOpenSearch1.1](A.04.TGR4.conformtoOpenSearch1.1.md)    | TG     | Yes        | Ready for review    |
| [A.05.IR221.TGR5.feedTitle](A.05.IR221.TGR5.feedTitle.md)    | TG     | Yes        | Ready for review    |
| [A.06.IR511.TGR6.linkToMetadataForTheService](A.06.IR511.TGR6.linkToMetadataForTheService.md)  | TG  | Yes  | Ready for review    |
| [A.07.TGR7.selfreference](A.07.TGR7.selfreference.md)  | TG     | Yes        | Ready for review    |
| [A.08.IR222.TGR8.linktoOpenSearchDescription](A.08.IR222.TGR8.linktoOpenSearchDescription.md)  | TG     | Yes        | Ready for review |
| [A.09.TGR9.feedid](A.09.TGR9.feedid.md)  | TG     | Yes        | Ready for review    |
| [A.10.IR221.TGR10.rightselement](A.10.IR221.TGR10.rightselement.md)   | TG     | Yes        | Ready for review    |
| [A.11.IR221.TGR11.updatedelement](A.11.IR221.TGR11.updatedelement.md) | TG     | Yes        | Ready for review    |
| [A.12.IR221.TGR12.contactinformation](A.12.IR221.TGR12.contactinformation.md) | TG     | Yes        | Ready for review    |
| [A.13.IR221.TGR13.datasetidentifiers](A.13.IR221.TGR13.datasetidentifiers.md) | TG     | Yes        | Ready for review    |
| [A.14.IR221.TGR14.linksToDatasetMetadata](A.14.IR221.TGR14.linksToDatasetMetadata.md) | TG     | Yes        | Ready for review    |
| [A.15.TGR15.linkToDatasetFeed](A.15.TGR15.linkToDatasetFeed.md) | TG | Yes | Ready for review |
| TGR 16 | TG | No | - |
| [A.16.TGR17.entryHasId](A.16.TGR17.entryHasId.md) | TG | Yes | Ready for review |
| [A.17.TGR18.entryTitle](A.17.TGR18.entryTitle.md) | TG | Yes | Ready for review |
| [A.18.TGR19.entryUpdated](A.18.TGR19.entryUpdated.md) | TG | Yes | Ready for review |
| [A.19.IR224.TGR20.entryCRS](A.19.IR224.TGR20.entryCRS.md) | TG | Yes | Ready for review |
| [A.20.IR224.TGR21.datasetFeedTitle](A.20.IR224.TGR21.datasetFeedTitle.md) | TG | Yes | Ready for review |
| [A.21.TGR22.datasetFeedId](A.21.TGR22.datasetFeedId.md) | TG | Yes | Ready for review |
| [A.22.IR221.TGR23.datasetFeedRights](A.22.IR221.TGR23.datasetFeedRights.md) | TG | Yes | Ready for review |
| [A.23.IR221.TGR24.datasetFeedUpdated](A.23.IR221.TGR24.datasetFeedUpdated.md) | TG | Yes | Ready for review |
| [A.24.IR221.TGR25.datasetFeedContactinformation](A.24.IR221.TGR25.datasetFeedContactinformation.md) | TG | Yes | Ready for review |
| [A.25.IR31.TGR26.datasetFeedDownloadLink](A.25.IR31.TGR26.datasetFeedDownloadLink.md) | TG | Yes | Ready for review |
| [A.26.IR313.TGR27.separateEntriesCRSFormat](A.26.IR313.TGR27.separateEntriesCRSFormat.md) | TG | Yes | Draft |
| [A.27.IR4.TGR28.spatialObjectType](A.27.IR4.TGR28.spatialObjectType.md) | TG | Yes | Draft |
| [A.28.IR31.TGR29.datasetFeedDownloadLinkDetails](A.28.IR31.TGR29.datasetFeedDownloadLinkDetails.md) | TG | Yes | Draft |
| TGR 30 | TG | No | - |
| [A.29.IR311.TGR31.languageForDownloadLink](A.29.IR311.TGR31.languageForDownloadLink.md) | TG | Yes | Draft |
| [A.30.TGR32.downloadMultipleFiles](A.30.TGR32.downloadMultipleFiles.md) | TG | Yes | Ready for review |
| [A.31.TGR33.downloadMultipleFilesGuidance](A.31.TGR33.downloadMultipleFilesGuidance.md) | TG | Yes | Ready for review |
| [A.32.TGR34.INSPIREmediaTypesOnly](A.32.TGR34.INSPIREmediaTypesOnly.md) | TG | Yes | Ready for review |
| [A.33.IR224.IR313.TGR35.categoryLabelCRS](A.33.IR224.IR313.TGR35.categoryLabelCRS.md) | TG | Yes | Ready for review |
| TGR 36 | TG | No | Not testable |
| TGR 37 | TG | No | Not testable |
| TGR 38 | TG | No | Not testable |
| [A.34.IR222.TGR39.provideOpenSearchDescription](A.34.IR222.TGR39.provideOpenSearchDescription.md)  | TG | No | Ready for review |
| [A.35.TGR40.openSearchSelfreference](A.35.TGR40.openSearchSelfreference.md)  | TG | Yes | Ready for review |
| [A.36.TGR41.openSearchGenericSearchQueries](A.36.TGR41.openSearchGenericSearchQueries.md)  | TG | Yes | Ready for review |
| [A.37.IR4.TGR42.openSearchUrlDescribeSpatialDataset](A.37.IR4.TGR42.openSearchUrlDescribeSpatialDataset.md)  | TG | Yes | Ready for review |
| [A.38.IR3.TGR43.openSearchUrlGetSpatialDataset](A.38.IR3.TGR43.openSearchUrlGetSpatialDataset.md)  | TG | Yes | Ready for review |
| [A.39.IR3.IR4.TGR44.openSearchQueryExample](A.39.IR3.IR4.TGR44.openSearchQueryExample.md)  | TG | Yes | Ready for review |
| [A.40.IR311.IR411.TGR45.openSearchLanguages](A.40.IR311.IR411.TGR45.openSearchLanguages.md) | TG | Yes | Ready for review |

## Open issues
