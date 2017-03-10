# Conformance class: Pre-defined Atom (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Download Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/download-service/3.1).

## Standardization target type

Atom download service feed with sub-feeds for data sets

## Dependencies <a name="dep"/>

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the download service, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ATOM](#ref_atom) | n/a | n/a |
| [OpenSearch](#ref_opensearch) | n/a | n/a |
| [GeoRSS Simple](#ref_georss_simple) | n/a | n/a |

Note that it was decided that conformance to third-party specifications will be expressed as a dependency to the relevant conformance class(es) in the abstract test suites. Deciding which executable test suites (ETS) to use for this will be decided during the implementation of the INSPIRE ETSs. INSPIRE will not develop its own ETSs for third-party specifications, but instead rely on passing external ETSs (e.g. OGC CITE tests) where available or rely on self-declaration. 

However, where no robust third-party ETS is known, an INSPIRE ATS may include basic tests (e.g. validation against an XML or RELAX-NG schema). In this case the [basic schema validation test](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/schema-validation) has been added.

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [OpenSearch](#ref_opensearch) | n/a | OpenSearch description | n/a |
 
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
| 1     | Datasets as individual entries       | [Separate dataset individual Atom service feed](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-entry-per-dataset) | n/a |
| 2     | Atom specification conformance       | [Schema validation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/schema-validation) | n/a |
| 3     | GeoRSS Simple conformance            | [Schema validation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/schema-validation) | n/a |
| 4     | OpenSearch conformance               | [Schema validation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/schema-validation) | n/a |
| 5     | Download Service Feed title          | [Provide a title element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-title) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 6     | Metadata record link for service     | [Provide link to metadata record for Download Service](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-link-to-metadata-record) | [IR NS](#ref_IR_NS), M1, section 2.2.1; [IR MD](#ref_IR_MD), section 2.2.4 |
| 7     | Download Service Feed self reference | [Download Service feed self-reference link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-self-reference-link) | n/a |
| 8     | OpenSearch Description link          | [Download Service feed link OpenSearch Description document](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-link-opensearch-description-document) |[IR NS](#ref_IR_NS), M1, section 2.2.2|
| 9     | Download Service Feed ID             | [Download Service feed HTTP URI](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-id) | n/a |
| 10    | Download Service Rights     | [Download Service feed rights element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-rights-element) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 11    | Download Service Updated    | [Download Service feed updated element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-updated-element) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 12    | Download Service Author     | [Download Service feed contact information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-contact-information) |[IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 13    | Spatial Data Set identifiers in Service Feed | [Download Service feed dataset identifiers](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-dataset-identifiers) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 14    | Dataset metadata record links in Service Feed | [Download Service feed links dataset metadata records](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-links-dataset-metadata-records) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 15    | Dataset Feed links in Service Feed   | [Download Service feed links dataset feed](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-links-dataset-feed) | n/a |
| 16    | WFS Capabilities document link       | [Download Service feed link to WFS Capabilities document](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-wfs-link) ||
| 17    | Dataset Feed ID in Service Feed      | [Download Service feed identifiers](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-identifiers) |n/a|
| 18    | Dataset Feed title in Service Feed   | [Download Service feed title](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-entry-titles) |n/a|
| 19    | Dataset Feed Updated element in Service Feed | [Download Service feed updated element date](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-updated-element-date) |n/a|
| 20    | Dataset CRS category elements in Service Feed | [Download Service feed CRS information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-crs-information) | [IR NS](#ref_IR_NS), M1, section 2.2.4|
| 21    | Dataset Feed title in Dataset Feed   | [Dataset Feed title](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-title) | [IR NS](#ref_IR_NS), M1, section 2.2.4|
| 22    | Dataset Feed ID in Dataset Feed      | [Dataset feed HTTP URI](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-id) |n/a|
| 23    | Dataset Feed Rights in Dataset Feed  | [Dataset feed rights element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-rights-element) | [IR NS](#ref_IR_NS), M1, section 2.2.1 |
| 24    | Dataset Updated in Dataset Feed      | [Dataset feed updated element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-updated-element) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 25    | Dataset Author in Dataset Feed       | [Dataset feed contact information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-contact-information) | [IR NS](#ref_IR_NS), M1, section 2.2.1|
| 26    | Dataset content entry                | [Dataset feed link download dataset](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-download-dataset) | [IR NS](#ref_IR_NS), M1, section 3.1|
| 27    | Dataset format/CRS specific content entries | [Separate entries for each format/CRS combination](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-entries) | [IR NS](#ref_IR_NS), M1, section 3.1.3 |
| 28    | Dataset Spatial Object Type link     | [Links for Spatial Object Types](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-links-spatial-object-types) | [IR NS](#ref_IR_NS), M1, section 4|
| 29    | Dataset entry content links          | [Dataset feed link download dataset](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-download-dataset) | [IR NS](#ref_IR_NS), M1, section 3.1 |
| 30    | Dataset entry content media type     | [Use INSPIRE media-types only](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-media-type) | n/a |
| 31    | Dataset entry content language       | [Language for download link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-dataset-language) | [IR NS](#ref_IR_NS), M1, section 3.1.1 |
| 32    | Sectioned dataset entry links        | [Multiple links for multiple physical files](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-multiple-files) |n/a|
| 33    | Sectioned dataset structure          | [Provide guidance for downloading multiple physical files](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-multiple-files-description) |n/a|
| 34    | Only INSPIRE media types allowed     | [Use INSPIRE media-types only](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-media-type) |n/a|
| 35    | Dataset CRS category elements in Dataset Feed | [Each entry has CRS information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-crs) |[IR NS](#ref_IR_NS), M1, section 3.1.3|
| 36    | Alternate languages in Service Feed  | Requirement always met | n/a |
| 37    | Language request parameter           | Requirement always met | n/a |
| 38    | Alternate language feed interlinking | [Language for download link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-dataset-language) | n/a |
| 39    | OpenSearch Description document      | [Download Service feed link OpenSearch Description document](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-link-opensearch-description-document) |[IR NS](#ref_IR_NS), M1, section 2.2.2|
| 40    | OpenSearch Description self reference | [OpenSearch Description URI to itself](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-uri-to-itself) |n/a|
| 41    | OpenSearch Generic search results URL template | [OpenSearch Description URL generic search queries](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-url-generic-search-queries) |n/a|
| 42    | OpenSearch Describe Spatial Data Set Operation template | [OpenSearch Description URL Describe Spatial Dataset operation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-url-describe-spatial-dataset-operation) | [IR NS](#ref_IR_NS), M1, section 4|
| 43    | OpenSearch Get Spatial Data Set Operation template | [OpenSearch Description one URL Get Spatial Dataset operation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-one-url-get-spatial-dataset-operation) |n/a|
| 44    | OpenSearch Spatial Data Set IDs as example queries | [OpenSearch Description Query examples for each dataset](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-query-examples-for-each-dataset) | [IR NS](#ref_IR_NS), M1, section 4|
| 45    | OpenSearch supported languages       | [OpenSearch Description provides languages](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-provides-languages) |[IR NS](#ref_IR_NS), M1, section 4.1.1|

## Tests

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Download Service Feed contact information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-contact-information) | ready for review |
| [Download Service Feed CRS information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-crs-information) | ready for review |
| [Download Service Feed dataset identifiers](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-dataset-identifiers) | ready for review |
| [Download Service Feed HTTP URI](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-id) | ready for review |
| [Download Service Feed identifiers](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-identifiers) | ready for review |
| [Download Service Feed link OpenSearch Description document](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-link-opensearch-description-document) | ready for review |
| [Download Service Feed link to WFS Capabilities document](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-wfs-link) | ready for review |
| [Download Service Feed links dataset feed](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-links-dataset-feed) | ready for review |
| [Download Service Feed links dataset metadata records](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-links-dataset-metadata-records) | ready for review |
| [Download Service Feed rights element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-rights-element) | ready for review |
| [Download Service Feed self-reference link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-self-reference-link) | ready for review |
| [Download Service Feed title](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-entry-titles) | ready for review |
| [Download Service Feed updated element date](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-updated-element-date) | ready for review |
| [Download Service Feed updated element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-updated-element) | ready for review |
| [Download Service Feed provide a title element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-title) | ready for review |
| [Download Service Feed provide link to metadata record for Download Service](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-link-to-metadata-record) | ready for review |
| [Download Service Feed separate dataset individual Atom service feed](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/download-service-feed-entry-per-dataset) | ready for review |
| [Dataset Feed contact information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-contact-information) | ready for review |
| [Dataset Feed HTTP URI](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-id) | ready for review |
| [Dataset Feed link download dataset](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-download-dataset) | ready for review |
| [Dataset Feed rights element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-rights-element) | ready for review |
| [Dataset Feed title](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-title) | ready for review |
| [Dataset Feed updated element](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-updated-element) | ready for review |
| [Dataset Feed each entry has CRS information](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-crs) | ready for review |
| [Dataset Feed language for download link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-dataset-language) | ready for review |
| [Dataset Feed links for Spatial Object Types](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-links-spatial-object-types) | ready for review |
| [Dataset Feed multiple links for multiple physical files](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-multiple-files) | ready for review |
| [Dataset Feed separate entries for each format/CRS combination](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-entries) | ready for review |
| [Dataset Feed use INSPIRE media-types only](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-link-media-type) | ready for review |
| [Dataset Feed provide guidance for downloading multiple physical files](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-multiple-files-description) | ready for review |
| [OpenSearch Description one URL Get Spatial Dataset operation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-one-url-get-spatial-dataset-operation) | ready for review |
| [OpenSearch Description provides languages](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-provides-languages) | ready for review |
| [OpenSearch Description Query examples for each dataset](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-query-examples-for-each-dataset) | ready for review |
| [OpenSearch Description URI to itself](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-uri-to-itself) | ready for review |
| [OpenSearch Description URL Describe Spatial Dataset operation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-url-describe-spatial-dataset-operation) | ready for review |
| [OpenSearch Description URL generic search queries](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/opensearch-description-url-generic-search-queries) | ready for review |
| [Schema validation](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/schema-validation) | ready for review |


## Open issues

* Is it allowed for more than one Download Service Feed to point to the same Dataset Feed? If yes, and if these Download Service Feeds contain different entries pointing to this Dataset Feed, which parent feed should be used for validation? One example for the possible conflict would be different CRS categories in the Download Service Feed entries.

* Should it be allowed for the Dataset Feed to additionally contain download links to files containing the data in other CRSes than the ones mentioned in it's parent Download Service Feed, or should the CRS (category) list in the Download Service Feed entry and the corresponding Dataset Feed match exactly?

* Is the hreflang attribute mandatory in the Dataset Feed link entries even if the data is provided only in a single language? If so, the test [Language for download link](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/dataset-feed-dataset-language) is not automatically testable and the should be removed.

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
