# Use INSPIRE media-types only

**Purpose**: Only media types listed in the INSPIRE media-types register must be used.

**Prerequisites**

**Test method**

* Get all media types from the INSPIRE register at http://inspire.ec.europa.eu/media-types/
* For each [media-type](#mediatypes) used in [alternate links](#alternatelinks), test if it that is listed in the INSPIRE register

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirements 30, 34

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
media-type <a name="mediatype"></a> | //atom:link[@rel='alternate']/@type
alternate links <a name="alternatelinks"></a> | //atom:link[@rel='alternate']
