# Conform to the GeoRSS-simple specification

**Purpose**: 

All feeds must conform to the GeoRSS Simple specification 

**Test method**

* validate the Atom service feed to [GeoRSS-Simple schema version 1.1](http://www.georss.org/xml/1.1/georss.xsd)
* for each [link to an Atom dataset feed](#atom_dataset_feed_link) in the service feed, resolve the link the referenced Atom feed and validate that to [GeoRSS-Simple schema version 1.1](http://www.georss.org/xml/1.1/georss.xsd)

**Reference(s)**: 

* TG, Req 3
* [GeoRSS-Simple schema version 1.1](http://www.georss.org/xml/1.1/georss.xsd)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to an Atom dataset feed <a name="atom_dataset_feed_link"></a> | //atom:entry/atom:link[@rel='alternate' and @type='application/atom+xml']