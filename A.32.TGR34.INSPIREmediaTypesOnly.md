# Use INSPIRE media-types only

**Purpose**: 

Only media types listed in the INSPIRE media-types register must be used.

**Test method**

* Get all media types from the INSPIRE register at http://inspire.ec.europa.eu/media-types/
* For each [media-type](#mediatypes) used in [alternate links](#alternatelinks), test if it that is listed in the INSPIRE register

**Reference(s)**: 

* TG, Req 34

**Test type**: 

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
media-type <a name="mediatype"></a> | //atom:link[@rel='alternate']/@type
alternate links <a name="alternatelinks"></a> | //atom:link[@rel='alternate']