# Schema validation

**Purpose**: All feeds must conform to the Atom specification (RFC 4287) and the GeoRSS simple specification. The referenced OpenSearch description documents must conform to the OpenSearch specification. This is expressed by the dependencies of the "Pre-defined Atom" conformance class to these specifications. As no Abstract Test Suite for those specifications are known and comprehensive validation of third party specifications is out-of-scope for an INSPIRE conformance class, this test case is intended to perform basic validation of the Atom and OpenSearch documents of the download service in order prepare for the specific test cases of this conformance class.

**Prerequisites**

**Test method**

* Validate the Atom service feed:
  * Validate the feed against the Relax NG schema in the [Atom specification](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_atom) (or an equivalent test).
  * Validate any XML elements in the [GeoRSS Simple](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_georss_simple) namespace against http://www.georss.org/xml/1.1/georss.xsd (or an equivalent test; since only georss:point/polygon/box may be used, those elements could be examined directly for the number of values - 2 in point, etc. - and the range of the lat/lon values). 
* Retrieve the resource at the URI in the [link to the OpenSearch Description](#opensearchlink) to get the OpenSearch Description. Validate the OpenSearch Description using a Relax NG or XML schema (or an equivalent test). 
* For each [link to an Atom dataset feed](#atom_dataset_feed_link) in the service feed, retrieve the resource at that URL and validate it against the same assertions as the service feed.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL,) Requirements 2, 3, 4
* [Atom](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_atom)
* [GeoRSS Simple](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_georss_simple)
* [OpenSearch](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_opensearch)

**Test type**: Automated

**Notes**

Note that it was decided that conformance to third-party specifications will be expressed as a dependency to the relevant conformance class(es) in the abstract test suites. Deciding which executable test suites (ETS) to use for this will be decided during the implementation of the INSPIRE ETSs. INSPIRE will not develop its own ETSs for third-party specifications, but instead rely on passing external ETSs (e.g. OGC CITE tests) where available or rely on self-declaration. However, where no robust third-party ETS is known, an INSPIRE ATS may include basic tests (e.g. validation against an XML or RELAX-NG schema). This is the purpose of this test case.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to an Atom dataset feed <a name="atom_dataset_feed_link"></a> | //atom:entry/atom:link[@rel='alternate' and @type='application/atom+xml']
link to the OpenSearch Description <a name="opensearchlink"></a> | /atom:feed/atom:link[@rel='search' and @type='application/opensearchdescription+xml']/@href
