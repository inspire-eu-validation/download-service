# Conformance class: Direct WFS (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Download Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/download-service/3.1).

## Standardization target type

OGC web service (WFS 2.0.0)

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the view service, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [WFS 2.0.0](#ref_WFS) | Basic WFS | n/a |
| [WFS 2.0.0](#ref_WFS) | HTTP GET | n/a |
| [FES 2.0.0](#ref_FES) | Ad-hoc Query | n/a |
| [FES 2.0.0](#ref_FES) | Resource Identification | n/a |
| [FES 2.0.0](#ref_FES) | Minimum Standard Filter | n/a |
| [FES 2.0.0](#ref_FES) | Minimum Spatial Filter | n/a |
| [FES 2.0.0](#ref_FES) | Minimum Temporal Filter | n/a |
| [FES 2.0.0](#ref_FES) | Minimum XPath | n/a |

### Indirect dependencies

none
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| TG DL <a name="ref_TG_DL"></a>   | [Technical Guidance for the implementation of INSPIRE Download Services 3.1](http://inspire.ec.europa.eu/documents/Network_Services/Technical_Guidance_Download_Services_v3.1.pdf)
| WFS 2.0 <a name="ref_WFS"></a> | [OpenGIS Web Feature Service 2.0 Interface Standard (also ISO 19142)](http://portal.opengeospatial.org/files/?artifact_id=39967)
| FES 2.0 <a name="ref_FES"></a> | [OpenGIS Filter Encoding 2.0 Encoding Standard](http://portal.opengeospatial.org/files/?artifact_id=39968)

## TG Requirement coverage

Based on requirement numbering in [TG VS](#ref_TG_VS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 61     | ISO 19142 HTTP GET compliance        | OGC WFS 2.0.0, A.1.5 HTTP GET      | n/a |
| 62     | ISO 19142 Basic WFS compliance       | OGC WFS 2.0.0, A.1.2 Basic WFS      | n/a |
| 63     | ISO 19143 Ad hoc Query               | OGC FES 2.0, A.2 Test cases for ad hoc query | n/a |
| 64     | ISO 19143 Resource Identification    | OGC FES 2.0, A.4 Test cases for resource identification | n/a |
| 65     | ISO 19143 Minimum Standard Filter    | OGC FES 2.0, A.5 Test cases for minimum standard filter | n/a |
| 66     | ISO 19143 Minimum Spatial Filter     | OGC FES 2.0, A.7 Test cases for minimum spatial filter | n/a |
| 67     | ISO 19143 Minimum Temporal Filter    | OGC FES 2.0, A.9 Test cases for minimum temporal filter | n/a |
| 68     | ISO 19143 Minimum XPath              | OGC FES 2.0, A.14 Test cases for XPath | n/a |

*Note*: These requirements are only for fulfilling the INSPIRE Download Service parts B & C. For a complete INSPIRE compliant Download Service, the additional requirements for the part A still need to be covered either by [Atom/OpenSearch](http://inspire.ec.europa.eu/id/ats/download-services/3.1/atom-pre-defined) or
the [predefined dataset WFS](http://inspire.ec.europa.eu/id/ats/download-services/3.1/wfs-pre-defined) CC.

## Tests

This conformance class does not specify any requirements in addition to the dependencies to conformance classes specified by the OGC standard documents [WFS 2.0](#ref_WFS) and [FES 2.0](#ref_FES). As a consequence, there are no INSPIRE specific test cases for this conformance class.