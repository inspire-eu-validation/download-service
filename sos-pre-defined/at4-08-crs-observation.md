# CRS Observation

**Purpose**: To download the data in a specific supported CRS, this must be included as parameter in the GetObservation request. If the CRS is unsupported, an exception will be raised.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* For every [Observation Offering](#observationOffering):

    * Send a GetObservation request with parameter 'crs' equal to [Default CRS](#defaultcrs).

        * Check if GetObservation response is correct.

    * For every [Other CRS](#othercrs):

        * Send a GetObservation request with parameter 'crs' equal to [Other CRS](#othercrs).

            * Check if GetObservation response is correct.

* Send a GetObservation request for an unsupported Coordinate Reference System.

  * Check if the service response is an ExceptionReport.

* If any of the validations fails, the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirement 4.8
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**

The multiplicity of [Observation Offering](#observationOffering) is 0 to n.

The multiplicity of [Default CRS](#defaultcrs) is 1.

The multiplicity of [Other CRS](#othercrs) is 0 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering |
| Default CRS <a name="defaultcrs"></a> | swes:extensions/inspire_dls:SupportedCRS/inspire_dls:DefaultCRS |
| Other CRS <a name="othercrs"></a> | swes:extensions/inspire_dls:SupportedCRS/inspire_dls:OtherCRS |