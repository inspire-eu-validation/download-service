# Observations Offerings Language Namespace and CRS

**Purpose**: Test that in the ObservationOfferings section of the getCapabilities response exits the Supported Languages, Namespaces and CRS nodes.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* Check the existence of [Observation Offering](#observationOffering) node. Its multiplicity is 0 to n. If it exists, for every observation:

  * Check if child element [Supported Languages](#supportedLanguages) exists.

  * Check if child element [Namespaces](#namespaces) exists.

  * Check if child element [CRS](#crs) exists.

* If ObservationOffering does not exist or any validation fails then the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.7
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering |
| Supported Languages <a name="supportedLanguages"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_common:SupportedLanguages |
| Namespaces <a name="namespaces"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_dls:SpatialDataSetIdentifier/inspire_common:Namespace |
| CRS <a name="crs"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_dls:SupportedSupportedCRS |