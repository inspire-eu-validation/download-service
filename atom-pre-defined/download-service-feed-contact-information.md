# Download Service feed contact information

**Purpose**: The Download Service feed must provide contact information about the individual or organisation responsible for the feed. The [author name](#authorname) and [email address](#emailaddress) shall be provided.

**Prerequisites**

**Test method**

* the [author name](#authorname) must be non-empty text; the text content must include at least one alpha-numeric letter.
* the [email address](#emailaddress) must be non-empty text; the text content must be a correclty formatted email address.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 12


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
author name <a name="authorname"></a>| /atom:feed/atom:author/atom:name
email address <a name="emailaddress"></a> | /atom:feed/atom:author/atom:email
