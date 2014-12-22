ats-download-atom
=================

Abstract Test Suite for Atom Implementation of Pre-defined Dataset Download Service of INSPIRE Download Services Technical Guidance 

References
* [INSPIRE Download Services Technical Guidance version 3.1](http://inspire.ec.europa.eu/documents/Network_Services/Technical_Guidance_Download_Services_v3.1.pdf)
* [COMMISSION REGULATION (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02009R0976-20101228&from=EN)

*Note*: This ATS is in draft stage, none of the tests have an official INSPIRE MIG approval.

This Conformance Class contains the following tests:

| Identifier                                                        | Origin | Mechanical | Status   |
| ----------------------------------------------------------------- | ------ | ---------- | -------- |
| [A.01.TGR1.separatedatasets](A.01.TGR1.separatedatasets.md)    | TG     | Yes        | Draft    |
| [A.02.TGR2.conformtoAtomSpecification](A.02.TGR2.conformtoAtomSpecification.md)    | TG     | Yes        | Draft    |
| [A.03.TGR3.conformtoGeoRSS-Simple](A.03.TGR3.conformtoGeoRSS-Simple.md)    | TG     | Yes        | Draft    |
| [A.04.TGR4.conformtoOpenSearch1.1](A.04.TGR4.conformtoOpenSearch1.1.md)    | TG     | Yes        | Draft    |
| [A.05.IR221.TGR5.feedTitle](A.05.IR221.TGR5.feedTitle.md)    | TG     | Yes        | Draft    |
| [A.06.IR511.TGR6.linkToMetadataForTheService](A.06.IR511.TGR6.linkToMetadataForTheService.md)  | TG  | Yes  | Draft    |
| [A.07.TGR7.selfreference](A.07.TGR7.selfreference.md)  | TG     | Yes        | Draft    |
| [A.08.IR222.TGR8.linktoOpenSearchDescription](A.08.IR222.TGR8.linktoOpenSearchDescription.md)  | TG     | Yes        | Draft | 
| [A.09.TGR9.feedid](A.09.TGR9.feedid.md)  | TG     | Yes        | Draft    |
| [A.10.IR221.TGR10.rightselement](A.10.IR221.TGR10.rightselement.md)   | TG     | Yes        | Draft    |
| [A.11.IR221.TGR11.updatedelement](A.11.IR221.TGR11.updatedelement.md) | TG     | Yes        | Draft    |
| [A.12.IR221.TGR12.contactinformation](A.12.IR221.TGR12.contactinformation.md) | TG     | Yes        | Draft    |
| [A.13.IR221.TGR13.datasetidentifiers](A.13.IR221.TGR13.datasetidentifiers.md) | TG     | Yes        | Draft    |
| [A.14.IR221.TGR14.linksToDatasetMetadata](A.14.IR221.TGR14.linksToDatasetMetadata.md) | TG     | Yes        | Draft    |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
atom           | http://www.w3.org/2005/Atom
georss         | http://www.georss.org/georss
gmd | http://www.isotc211.org/2005/gmd
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
os             | http://a9.com/-/spec/opensearch/1.1/
xlink          | http://www.w3.org/1999/xlink
