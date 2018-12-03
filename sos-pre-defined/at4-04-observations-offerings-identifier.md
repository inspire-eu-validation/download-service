# Observations Offerings Identifier

**Purpose**: Test that the Observations Offerings have an Identifier, and it is a URI according to [OGC SWE Service Model]

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

    * For every [Observation Offering](#observationOffering) node:

        * Check if child element [Identifier](#identifier) exists for every observation. Its value SHALL be a URI according to [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476).

    * If any validation fails then the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.4
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**

The multiplicity of [Observation Offering](#observationOffering) is 0 to n.

The multiplicity of [Identifier](#identifier) is 1 for each [Observation Offering](#observationOffering).

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering |
| Identifier <a name="identifier"></a> | /sos:Capabilities/*\/sos:Contents/swes:offering/sos:ObservationOffering/swes:identifier |