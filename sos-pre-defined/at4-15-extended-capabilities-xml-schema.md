# Extended Capabilities XML Schema

**Purpose**: Test that the capabilities document is schema valid according to INSPIRE online schema repository

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

* Check if the [ExtendedCapabilities](#extendedCapabilities) element and it's children according to the XML Schema definition for the SOS INSPIRE extendedCapabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd

* If validation fails, the test fails

**Reference(s)**

* [INS TG SOS](http://inspire.ec.europa.eu/id/document/tg/download-sos/1.0), Requirements 4.15

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/sos-tg-1.0/sos-pre-defined/README#namespaces).

| Abbreviation                                               |  XPath expression |
| ---------------------------------------------------------- | ------------------------------------------------------------------------- |
| ExtendedCapabilities <a name="extendedCapabilities"></a>   | ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1] |