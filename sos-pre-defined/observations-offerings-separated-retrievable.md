# Observations Offerings Separated and Retrievable

**Purpose**: Check that the ObservationOfferings available in the service are retrievable using a GetObservation request.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.
* Check the existence of [Observation Offering](#observationOffering) node. Its multiplicity is 0 to n. If it exists
  * For every observation send a GetObservation request using the observation's [Identifier](#identifier).
    * Validate the GetObservation response.
* If ObservationOffering does not exist or any validation fails then the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.5
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering |
| Identifier <a name="identifier"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:identifier |