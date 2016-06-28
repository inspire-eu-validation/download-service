# Dataset feed contact information

**Purpose**:

The dataset feed must provide contact information about the individual or organisation responsible for the feed. The [author name](#authorname) and [email address](#emailaddress) must be provided.

 **Test method**

* the [author name](#authorname) must be non-empty text; the text content must include at least one alpha-numeric letter.
* the [email address](#emailaddress) must be non-empty text; the text content must be a correclty formatted email address.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 25


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
author name <a name="authorname"></a>| /atom:feed/atom:author/atom:name
email address <a name="emailaddress"></a> | /atom:feed/atom:author/atom:email
