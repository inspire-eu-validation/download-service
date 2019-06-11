# Conformance class: WCS Core (DRAFT)

This conformance class is part of the [Technical Guidance for the implementation of INSPIRE Download Services using Web Coverage Services (WCS)](https://inspire.ec.europa.eu/id/document/tg/download-wcs).

## Standardization target type

OGC WCS 2.0

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the download service.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [OGC WCS](#ref_OGC_WCS) | OGC WCS 2.0 Interface Standard – Core | n/a |

### Indirect dependencies

none
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN) |
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN) |
| INS TG WCS <a name="ref_INS_TG_WCS"></a>   | [Technical Guidance for the implementation of INSPIRE Download Services using Web Coverage Services (WCS)](https://inspire.ec.europa.eu/id/document/tg/download-wcs) |
| OGC WCS <a name="ref_OGC_WCS"></a> | [OGC WCS 2.0 Interface Standard – Core](https://www.opengeospatial.org/standards/wcs) |
| INS MDTG | [INSPIRE Metadata Implementing Rules](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf) |
| Web Service Common | [OGC 06-121r9, OGC Web Service Common Specification, version 2.0](https://www.opengeospatial.org/standards/common) |

## TG Requirement coverage

Based on requirement numbering in [INS TG WCS](#ref_INS_TG_WCS).

| Req#   | Description                          | Covered by test(s)                 |
| ------ | ------------------------------------ | ---------------------------------- |
| 1    | Conform to the OGC WCS 2.0 Conformance Class 'core WCS'| [OGC WCS](#ref_OGC_WCS) Core WCS
| 2    | Protocol bindings | [at02-protocol-bindings](./at02-protocol-bindings.md)
| 3    | Natural language fields | [at03-natural-language-fields](./at03-natural-language-fields.md)
| 4    | XML schema validation | [at04-xml-schema-validation](./at04-xml-schema-validation.md)
| 5    | Supported languages | [at05-supported-languages](./at05-supported-languages.md)
| 6    | Mandatory metadata elements | [at06-mandatory-metadata-elements](./at06-mandatory-metadata-elements.md)
| 7    | Language request empty and unsupported | [at07-language-request-empty-unsupported](./at07-language-request-empty-unsupported.md)
| 8    | List of supported languages | [at08-list-supported-languages](./at08-list-supported-languages.md)
| 9    | Response language | [at09-response-language](./at09-response-language.md)

## Tests
The Conformance class "TG Conformance WCS-MAN: Mandatory Download Operations" contains the following tests:

| Identifier                                                        | Type   | Status   |
| ----------------------------------------------------------------- | -------- | -------- |
| [at02-protocol-bindings](./at02-protocol-bindings.md) | Automated | ready for review |
| [at03-natural-language-fields](./at03-natural-language-fields.md) | Manual | ready for review |
| [at04-xml-schema-validation](./at04-xml-schema-validation.md) | Automated | ready for review |
| [at05-supported-languages](./at05-supported-languages.md) | None | ready for review |
| [at06-mandatory-metadata-elements](./at06-mandatory-metadata-elements.md) | Automated | ready for review |
| [at07-language-request-empty-unsupported](./at07-language-request-empty-unsupported.md) | Automated | ready for review |
| [at08-list-supported-languages](./at08-list-supported-languages.md) | Automated | ready for review |
| [at09-response-language](./at09-response-language.md) | Automated | ready for review |

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
wcs            | http://www.opengis.net/wcs/2.0
xlink          | http://www.w3.org/1999/xlink
