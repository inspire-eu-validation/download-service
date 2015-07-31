# Dataset feed contains the HTTP URI of the feed as id

**Purpose**:

The dataset feed must provide the HTTP URI of the feed as [feed id](#feedid).

 **Test method**

* compare the [feed id](#feedid) to the HTTP URI of the dataset feed, that is being tested currently

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 22
* [Atom](README.md#ref_atom)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed id <a name="feedid"></a> | /atom:feed/atom:id
