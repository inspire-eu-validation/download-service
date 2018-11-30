# CRS Observation

**Purpose**: Check that the observations may be served in different CRS. To download the data in a specific supported CRS it must be send as parameter in the GetObservation request. If the CRS is unsupported, an exception will be raised.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.
* For every [Observation Offering](#observationOffering)
  * Send a GetObservation request for every supported [CRS](#crs)
  * Validate GetObservation response is in the requested CRS
* Send a GetObservation request for an unsupported CRS
  * Validate the response is the corresponding unsupported CRS exception
* If any of the validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.8
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering |
| CRS <a name="crs"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:extensions/inspire_dls:SupportedSupportedCRS |