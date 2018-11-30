# Conformance class: Pre-defined SOS (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Download Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/download-service/3.1).

## Standardization target type

OGC web service (SOS 2.0)

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the download service.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [OGC SOS](#ref_OGC_SOS) | SOS Core | n/a |
| [FES 2.0.0](#ref_FES) | Query | n/a |

### Indirect dependencies

none
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN) |
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN) |
| INS TG SOS <a name="ref_INS_TG_SOS"></a>   | [Technical Guidance for implementing download services using the OGC Sensor Observation Service and ISO 19143 Filter Encoding](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0) |
| OGC SOS <a name="ref_OGC_SOS"></a> | [OGC 12-006 Sensor Observation Service Interface Standard](https://portal.opengeospatial.org/files/?artifact_id=47599) |
| FES 2.0 <a name="ref_FES"></a> | [OpenGIS Filter Encoding 2.0 Encoding Standard](http://portal.opengeospatial.org/files/?artifact_id=39968) |
| OGC SWE Service Model | [SWE Service Model Implementation Standard 2.0](http://portal.opengeospatial.org/files/?artifact_id=38476) |
| INS MDTG | [INSPIRE Metadata Implementing Rules](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf) |

## TG Requirement coverage

Based on requirement numbering in [INS TG SOS](#ref_INS_TG_SOS).

| Req#   | Description                          | Covered by test(s)                 |
| ------ | ------------------------------------ | ---------------------------------- |
| 4.1    | Conform to the OGC SOS Conformance Class 'SOS Core'| [OGC SOS](#ref_OGC_SOS) 14.1.1 SOS Core
| 4.2    | Conform to the OGC SOS Conformance Class 'Spatial Filtering Profile'| [OGC SOS](#ref_OGC_SOS) 14.5.1 SOS Spatial Filtering Profile 
| 4.3    | Conform to the OGC SOS Conformance Classes 'Core KVP Binding' and 'XML Encoding'| [OGC SOS](#ref_OGC_SOS) 14.6.1 XML Encoding and 14.6.2 KVP Binding Extension
| 4.4    | Observations Offerings Identifier | [at4-04-observations-offerings-identifier](./at4-04-observations-offerings-identifier.md)
| 4.5    | Observations Offerings Separated and Retrievable | [at4-05-observations-offerings-separated-retrievable](./at4-05-observations-offerings-separated-retrievable.md)
| 4.6    | Extended capabilities | [at4-06-extended-capabilities](./at4-06-extended-capabilities.md)
| 4.7    | Observations Offerings Language Namespace and CRS | [at4-07-observations-offerings-lang-namespace-crs](./at4-07-observations-offerings-lang-namespace-crs.md)
| 4.8    | CRS Observation | [at4-08-crs-observation](./at4-08-crs-observation.md)
| 4.9    | Language Capabilities Supported | [at4-09-language-capabilities-supported](./at4-09-language-capabilities-supported.md)
| 4.10   | Language Capabilities Request | [at4-10-language-capabilities-request](./at4-10-language-capabilities-request.md)
| 4.11   | Language Capabilities Parameter | [at4-11-language-capabilities-parameter](./at4-11-language-capabilities-parameter.md)
| 4.12   | Language Capabilities Default | [at4-12-language-capabilities-default](./at4-12-language-capabilities-default.md)
| 4.13   | Language Capabilities Response | [at4-13-language-capabilities-response](./at4-13-language-capabilities-response.md)
| 4.14   | Language Capabilities List | [at4-14-language-capabilities-list](./at4-14-language-capabilities-list.md)
| 4.15   | Extended Capabilities XML Schema | [at4-15-extended-capabilities-xml-schema](./at4-15-extended-capabilities-xml-schema.md)

## Tests
The Conformance class "Pre-defined SOS: Implement Pre-defined Dataset Download Service (“Part A”) using Sensor Observation Service and ISO 19143 Filter Encoding" contains the following tests:

| Identifier                                                        | Type   | Status   |
| ----------------------------------------------------------------- | -------- | -------- |
| [at4-04-observations-offerings-identifier](./at4-04-observations-offerings-identifier.md) | Automated | ready for review |
| [at4-05-observations-offerings-separated-retrievable](./at4-05-observations-offerings-separated-retrievable.md) | Automated | ready for review |
| [at4-06-sos-pre-defined/extended-capabilities](./at4-06-sos-pre-defined/extended-capabilities.md) | Automated | ready for review |
| [at4-07-observations-offerings-lang-namespace-crs](./at4-07-observations-offerings-lang-namespace-crs.md) | Automated | ready for review |
| [at4-08-crs-observation](./at4-08-crs-observation.md) | Automated | ready for review |
| [at4-09-language-capabilities-supported](./at4-09-language-capabilities-supported.md) | Automated | ready for review |
| [at4-10-language-capabilities-request](./at4-10-language-capabilities-request.md) | Automated | ready for review |
| [at4-11-language-capabilities-parameter](./at4-11-language-capabilities-parameter.md) | Automated | ready for review |
| [at4-12-language-capabilities-default](./at4-12-language-capabilities-default.md) | Automated | ready for review |
| [at4-13-language-capabilities-response](./at4-13-language-capabilities-response.md) | Automated | ready for review |
| [at4-14-language-capabilities-list](./at4-14-language-capabilities-list.md) | Automated | ready for review |
| [at4-15-extended-capabilities-xml-schema](./at4-15-extended-capabilities-xml-schema.md) | Automated | ready for review |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
fes            | http://www.opengis.net/fes/2.0
gmd            | http://www.isotc211.org/2005/gmd
gml            | http://www.opengis.net/gml/3.2
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
ows            | http://www.opengis.net/ows/1.1
sos            | http://www.opengis.net/sos
xlink          | http://www.w3.org/1999/xlink
