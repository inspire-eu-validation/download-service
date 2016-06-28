Pre-defined WFS v3.1
====================

 Conformance Class for Pre-defined WFS v3.1

*Note*: This ATS is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

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
| 46     | ISO 19142 Simple WFS compliance      | OGC WFS 2.0.0, A.1.1 Simple WFS    | n/a |
| 47     | ISO 19143 Query compliance           | OGC FES 2.0, A.1 Test cases for query | n/a |
| 48     | ISO 19142 HTTP GET compliance        | OGC WFS 2.0.0, A.1.5 HTTP GET      | n/a |
| 49     | Use stored queries for datasets      | [Predefined Stored Query](predefined-stored-query.md) | |
| 50     | Stored queries for all available CRS/DataSetIdCode/DataSetIdnamespace/language combinations | [Predefined Stored Query](predefined-stored-query.md) | |
| 51     | Fixed stored query parameter names   | [Predefined Stored Query](predefined-stored-query.md) | |
| 52     | Separate service for each dataset    | | |
| 53     | INSPIRE metadata in extended Capabilities | [Service Metadata](service-metadata.md) | |
| 54     | List of supported languages          | [Provide Supported Languages](provide-supported-languages.md) | |
| 55     | User may select the language         | [Language affects capabilities](language-affects-capabilities.md) | |
| 56     | GetCapabilities LANGUAGE parameter   | [Language affects capabilities](language-affects-capabilities.md) | |
| 57     | Title & abstract fallback language   | [Provide Default Language](provide-default-language.md) | |
| 58     | ResponseLanguage element             | [Provide Response Language](provide-response-language.md) | |
| 59     | SupportedLanguages element           | [Provide Supported Languages](provide-supported-languages.md), [Provide default language](provide-default-language.md) | |
| 60     | Extended capabilities schema         | [Extended capabilities](extended-capabilities.md) | |

## Tests

The ATS for the TG Conformance Class 2: Pre-defined WFS: Implement Pre-Defined Dataset Download Service ("Part A") using ISO 19142 Web Feature Service and 19143 Filter Encoding contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Extended capabilities](extended-capabilities.md) | Ready for review |
| [Predefined Stored Query](predefined-stored-query.md) | Ready for review    |
| [Service Metadata](service-metadata.md)   | Ready for review    |
| [Language affects capabilities](language-affects-capabilities.md) | Ready for review |
| [Provide Response Language](provide-response-language.md)    | Ready for review    |
| [Provide Supported Languages](provide-supported-languages.md)   | Ready for review    |
| [Provide Default Language](provide-default-language.md) | Ready for review |

## Notes

<a name="ogccite">OGC's CITE</a> tests could be used to test conformance to the WFS standard. The CITE tests is useful for several TG requirements. Information on the test can be found at [http://cite.opengeospatial.org/](http://cite.opengeospatial.org/) and more specifically at [http://cite.opengeospatial.org/teamengine/about/wfs20/2.0.0/site/index.html](http://cite.opengeospatial.org/teamengine/about/wfs20/2.0.0/site/index.html).

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
fes | http://www.opengis.net/fes/2.0
gmd | http://www.isotc211.org/2005/gmd
gml | http://www.opengis.net/gml/3.2
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
ows | http://www.opengis.net/ows/1.1
wfs | http://www.opengis.net/wfs/2.0
xlink          | http://www.w3.org/1999/xlink
