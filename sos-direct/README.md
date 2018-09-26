# Conformance class: Direct SOS (DRAFT)

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
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| INS TG SOS <a name="ref_INS_TG_SOS"></a>   | [Technical Guidance for implementing download services using the OGC Sensor Observation Service and ISO 19143 Filter Encoding](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0) 
| OGC SOS <a name="ref_OGC_SOS"></a> | [OGC 12-006 Sensor Observation Service Interface Standard](https://portal.opengeospatial.org/files/?artifact_id=47599)
| FES 2.0 <a name="ref_FES"></a> | [OpenGIS Filter Encoding 2.0 Encoding Standard](http://portal.opengeospatial.org/files/?artifact_id=39968)

## TG Requirement coverage

Based on requirement numbering in [INS TG SOS](#ref_INS_TG_SOS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 5.1    | Implementations SHALL conform to the [OGC SOS] Conformance Class ‘SOS Core’ and meet TG Requirement 4.2, TG Requirement 4.3, and TG Requirement 4.6 to TG Requirement 4.15 | [OGC SOS](#ref_OGC_SOS) 14.1.1 SOS Core, [OGC SOS](#ref_OGC_SOS) 14.5.1 SOS Spatial Filtering Profile, [OGC SOS](#ref_OGC_SOS) 14.6.1 XML Encoding and 14.6.2 KVP Binding Extension, [Extended Capabilities](../sos-pre-defined/extended-capabilities), [Observations Offerings Language Namespace and CRS](../sos-pre-defined/observations-offerings-lang-namespace-crs), [CRS Observation](../sos-pre-defined/crs-observation), [Language Capabilities Supported](../sos-pre-defined/language-capabilities-supported), [Language Capabilities Request](../sos-pre-defined/language-capabilities-request), [Language Capabilities Parameter](../sos-pre-defined/language-capabilities-parameter), [Language Capabilities Default](../sos-pre-defined/language-capabilities-default), [Language Capabilities Response](../sos-pre-defined/language-capabilities-response), [Language Capabilities List](../sos-pre-defined/language-capabilities-list), [Extended Capabilities XML Schema](../sos-pre-defined/extended-capabilities-xml-schema) | |
| 5.2    | A Direct Access Download Service SHALL implement the GetObservationByID operation | [OGC SOS](#ref_OGC_SOS) 14.2.2 SOS Observation Retrieval By Id | |

## Tests
The Conformance class "Direct SOS: Implement Direct Access Download Service (“Parts A, B & C”) using Sensor Observation Service" is covered by the tests shown in the previous section. Therefore there is not specific tests for this conformance class.

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
