# Observations Offering Retrievable

**Purpose**: Check that the getCapabilities response lists the metadata asociated with the ObservationOfferings available in the service. The ObservationOffering groups a collection of observations produced by one procedure. The actual data can be accesed with the GetObservation request with an identifier parameter. This test checks the requeriments shown in the Reference section.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.
* Check the existence of [Observation Offering](#observationOffering) node. Its multiplicity is 0 to n. If it exists
  * Validate the child element [Identifier](#identifier) for every observation. Its value SHALL be a URI according to [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476).
  supported languages, namespaces
  * Validate the child element [Supported Languages](#supportedLanguages) for every observation.
  * Validate the child element [Namespaces](#namespaces) for every observation.
  * Validate the child element [CRS](#crs) for every observation.
  * For every observation send a GetObservation request using the observation's [Identifier](#identifier).
    * Validate the GetObservation response.
* If ObservationOffering does not exist or any validation fails then the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.4, 4.5, 4.7
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering |
| Identifier <a name="identifier"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:identifier |
| Supported Languages <a name="supportedLanguages"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_common:SupportedLanguages |
| Namespaces <a name="namespaces"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_dls:SpatialDataSetIdentifier/inspire_common:Namespace |
| CRS <a name="crs"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_dls:SupportedSupportedCRS |