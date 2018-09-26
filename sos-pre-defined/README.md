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

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 4.1    | Conform to the OGC SOS Conformance Class 'SOS Core'| [OGC SOS](#ref_OGC_SOS) 14.1.1 SOS Core | |
| 4.2    | Conform to the OGC SOS Conformance Class 'Spatial Filtering Profile'| [OGC SOS](#ref_OGC_SOS) 14.5.1 SOS Spatial Filtering Profile  | |
| 4.3    | Conform to the OGC SOS Conformance Classes 'Core KVP Binding' and 'XML Encoding'| [OGC SOS](#ref_OGC_SOS) 14.6.1 XML Encoding and 14.6.2 KVP Binding Extension | |
| 4.4    | According to [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476), the ObservationOffering identifier SHALL be a URI | [Observations Offerings Identifier](./observations-offerings-identifier) | |
| 4.5    | Each observation related spatial dataset SHALL be made available through separate SOS ObservationOfferings(s) and be retrievable through a GetObservation query | [Observations Offerings Separated and Retrievable](./observations-offerings-separated-retrievable) | |
| 4.6    | INSPIRE Metadata for the Download Service SHALL EITHER be linked to via an <inspire_common:MetadataURL> in an extended capabilities section, OR the extended capabilities section shall contain all the INSPIRE Metadata for the Download Service in accordance with the inspire_dls:ExtendedCapabilities schema | [Extended Capabilities](./extended-capabilities) | |
| 4.7    | For each data set, the information about supported languages, namespaces and CRSs SHALL be provided in the corresponding ObservationOffering section in the SOS Capabilities document | [Observations Offerings Language Namespace and CRS](./observations-offerings-lang-namespace-crs) | |
| 4.8    | A client may specify a specific CRS in a GetObservation request. If the requested CRS is contained in the list of supported CRS, the coordinates returned in the service response SHALL be in the requested CRS. If the requested CRS is not supported by the service, then a corresponding exception SHALL be returned | [CRS Observation](./crs-observation) | |
| 4.9    | A network service [Download Service] metadata response SHALL contain a list of the natural languages supported by the service. This list shall contain one or more languages that are supported | [Language Capabilities Supported](./language-capabilities-supported) | |
| 4.10   | A client may specify a specific language in a request. If the requested language is contained in the list of supported languages, the natural language fields of the service response SHALL be in the requested language. If the requested language is not supported by the service, then this parameter SHALL be ignored | [Language Capabilities Request](./language-capabilities-request) | |
| 4.11   | The name of the parameter to indicate the preferred language SHALL be “LANGUAGE”. The parameter values are based on ISO 639-2/B alpha 3 codes as used in [INS MDTG] | [Language Capabilities Parameter](./language-capabilities-parameter) | |
| 4.12   | If a client request specifies an unsupported language, or the parameter is absent in the request, the following fields SHALL be provided in the service default language: 'Description', 'Title', 'Abstract', 'Offering names' | [Language Capabilities Default](./language-capabilities-default) | |
| 4.13   | The Extended Capabilities shall indicate the response language used for the GetCapabilities-Response: Depending on the requested language the value of the <inspire_common:ResponseLanguage> corresponds to the current used language. If a supported language was requested, <inspire_common:ResponseLanguage> SHALL correspond to that requested language. If an unsupported language was requested or if no specific language was requested <inspire_common:ResponseLanguage> SHALL correspond to the service default language <inspire_common:DefaultLanguage> | [Language Capabilities Response](./language-capabilities-response) | |
| 4.14   | The Extended Capabilities SHALL contain the list of supported languages indicated in <inspire_common:SupportedLanguages>. This list of supported languages shall consist of 1. exactly one element <inspire_common:DefaultLanguage> indicating the service default language, and 2. zero or more elements <inspire_common:SupportedLanguage> to indicate all additional supported languages. Regardless of the response language, the list of supported languages is invariant for each GetCapabilities-Response | [Language Capabilities List](./language-capabilities-list) | |
| 4.15   | The Extended Capabilities SHALL use the XML Schema as defined in the INSPIRE online schema repository (http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd) | [Extended Capabilities XML Schema](./extended-capabilities-xml-schema) | |

## Tests
The Conformance class "Pre-defined SOS: Implement Pre-defined Dataset Download Service (“Part A”) using Sensor Observation Service and ISO 19143 Filter Encoding" contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Observations Offerings Identifier](./observations-offerings-identifier) | |
| [Observations Offerings Separated and Retrievable](./observations-offerings-separated-retrievable) | |
| [Extended Capabilities](./sos-pre-defined/extended-capabilities) | |
| [Observations Offerings Language Namespace and CRS](./observations-offerings-lang-namespace-crs) | |
| [CRS Observation](./crs-observation) | |
| [Language Capabilities Supported](./language-capabilities-supported) | |
| [Language Capabilities Request](./language-capabilities-request) | |
| [Language Capabilities Parameter](./language-capabilities-parameter) | |
| [Language Capabilities Default](./language-capabilities-default) | |
| [Language Capabilities Response](./language-capabilities-response) | |
| [Language Capabilities List](./language-capabilities-list) | |
| [Extended Capabilities XML Schema](./extended-capabilities-xml-schema) | |

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
