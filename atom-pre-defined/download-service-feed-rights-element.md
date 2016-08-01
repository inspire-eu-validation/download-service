# Download Service feed rights element

**Purpose**: The Download Service feed must provide information about rights or restrictions for that feed in the feed's [rights element](#rightselement).

**Prerequisites**

**Test method**

* the [rights element](#rightselement) must be non-empty text; the text content must include at least one alpha-numeric character.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 10

**Test type**: Automated

**Notes**

It is only possible to test for existence of an alphanumerical character; testing the contents of the element is not possible to implement without further specification

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
rights element <a name="rightselement"></a> | /atom:feed/atom:rights
