# Download Service feed: link to WFS Capabilities document

**Purpose**: In case of a 'hybrid implementation' using WFS for implementing direct access, a link shall be provided to the WFS Capabilities document. 

**Prerequisites**

**Test method**

This test case only applies, if the same data set is available as a WFS 2.0.0 Direct Access Download Service.

Check that the download service feed includes a link to the WFS Capabilities document with the "rel" attribute set to "related" and the "type" attribute set to "application/xml".

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 16

**Test type**: Manual

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
