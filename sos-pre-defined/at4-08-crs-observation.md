# CRS Observation

**Purpose**: Test that the observations may be served in different CRS. To download the data in a specific supported CRS it must be send as parameter in the GetObservation request. If the CRS is unsupported, an exception will be raised.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* For every [Observation Offering](#observationOffering):

  * Send a GetObservation request for every supported [CRS](#crs).

  * Check if GetObservation response is in the requested CRS.

* Send a GetObservation request for an unsupported CRS.

  * Check if the response is the corresponding unsupported CRS exception

* If any of the validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.8
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**

The multiplicity of [Observation Offering](#observationOffering) is 0 to n.

The multiplicity of [CRS](#crs) is 1 to n.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering |
| CRS <a name="crs"></a> | swes:extensions/inspire_dls:SupportedSupportedCRS |