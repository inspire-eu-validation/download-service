# Links for Spatial Object Types

**Purpose**: The dataset feed must contain an Atom link element for each INSPIRE Spatial Object Type in the dataset. The link must refer to the INSPIRE Registry unless the data does not conform to any Data Specification in which case a link to a local definition of the Spatial Object Type must be used instead. The value of the "rel" attribute of this element must be "describedby". For definitions in the INSPIRE registry the value of the "type" attribute must be "text/html".

**Prerequisites**

**Test method**

* test if the dataset feed contains at least one [link to a registry](#registrylink)

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 28

**Test type**: Automated

**Notes**

This test could als be considered a test for the IR section 2.2.4, metadata elements.

No check is done to see if it is a valid description / reference to the INSPIRE Registry. This can't be strictly tested at the moment, because data may not be harmonized (according to data specs) yet and then a different HTML description is allowed as well.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link to a registry <a name="registrylink"></a> | /atom:feed/atom:link[@rel='describedby' and @type='text/html']
