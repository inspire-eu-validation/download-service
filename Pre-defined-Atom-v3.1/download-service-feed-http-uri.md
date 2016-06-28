# Download Service feed HTTP URI 

**Purpose**:

The Download Service feed must provide the HTTP URI of the feed as [feed id](#feedid).

 **Test method**

* test that the [feed id](#feedid) is an HTTP URI
* resolve the [feed id](#feedid) and test if the returned document is the same as the Download Service feed that is being tested currently

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 9
* [Atom](REAME.md#ref_atom)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
feed id <a name="feedid"></a> | /atom:feed/atom:id
