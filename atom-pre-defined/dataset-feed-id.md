# Dataset feed HTTP URI

**Purpose**: The dataset feed must provide the HTTP URI of the feed as [feed id](#feedid).

**Prerequisites**

**Test method**

* test that the [feed id](#feedid) is an HTTP URI
* retrieve the resource at the [feed id](#feedid) and test if the returned document is the same as the dataset feed that is being tested currently

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 22
* [Atom](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_atom)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed id <a name="feedid"></a> | /atom:feed/atom:id
