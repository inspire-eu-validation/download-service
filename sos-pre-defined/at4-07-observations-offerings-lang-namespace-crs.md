# Observations Offerings Language Namespace and CRS

**Purpose**: Test that in the ObservationOfferings section of the getCapabilities response exits the Supported Languages, Namespaces and CRS nodes.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* For each [Observation Offering](#observationOffering) node:

  * Check if child element [Supported Languages](#supportedLanguages) exists.

  * Check if child element [Namespaces](#namespaces) exists.

  * Check if child element [CRS](#crs) exists.

* If ObservationOffering does not exist or any validation fails then the test fails.

**Reference(s)**:

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.7
* [OGC SWE Service Model](http://portal.opengeospatial.org/files/?artifact_id=38476)

**Test type**: Automated

**Notes**

The multiplicity of [Observation Offering](#observationOffering) is 0 to n.

The multiplicity of [Supported Languages](#supportedLanguages) is 1.

The multiplicity of [Namespaces](#namespaces) is 1.

The multiplicity of [CRS](#crs) is 1 to n.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

| Abbreviation                                               |  XPath expression (relative to /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering) |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| Observation Offering <a name="observationOffering"></a> | /sos:Capabilities/sos:contents/sos:Contents/swes:offering/sos:ObservationOffering |
| Supported Languages <a name="supportedLanguages"></a> | swes:extensions/inspire_common:SupportedLanguages |
| Namespaces <a name="namespaces"></a> | swes:extensions/inspire_dls:SpatialDataSetIdentifier/inspire_common:Namespace |
| CRS <a name="crs"></a> | swes:extensions/inspire_dls:SupportedSupportedCRS |