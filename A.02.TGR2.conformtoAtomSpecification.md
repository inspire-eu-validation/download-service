# Conform to the Atom specification

**Purpose**: 

All feeds must conform to the Atom specification RFC 4287

**Test method**

The Atom Download service feed and all entries for a Atom Dataset feeds must validate against the Atom specification [RFC 4287](http://tools.ietf.org/html/rfc4287).

* validate the Atom service feed to RFC 4287
* for each [link to an Atom dataset feed](#atom_dataset_feed_link) in the service feed, resolve the link the referenced Atom feed and validate that to RFC 4287

**Reference(s)**: 

* TG, Req 2
* [RFC 4287](http://tools.ietf.org/html/rfc4287)

**Test type**: Automated

**Notes**

There does not seem to be an official XML Schema that can be used directly. It might be needed to develop a schema, use another validator like the [W3C validator](http://validator.w3.org/feed/) and/or use the RELAX NG schema provided in the Atom specification. Note that the ATOM specifications allows any order for the elements. Before validating, the xml elements therefore must be shuffled to match the order chosen in the XML schema.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to an Atom dataset feed <a name="atom_dataset_feed_link"></a> | //atom:entry/atom:link[@rel='alternate' and @type='application/atom+xml']