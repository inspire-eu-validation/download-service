# Language for download link

**Purpose**:

Where alternative language representations of datasets are linked to, the \" [hreflang attribute](#hreflang) \" attribute of the [link](#downloadlink) element must be used to indicate the language of the target dataset as described in the Atom specification.

**Test method**

* test if the download [link](#downloadlink) provides the [hreflang attribute](#hreflang)

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 31
* [IR NS](README.md#ref_IR_NS), M1, section 3.1.1, Language parameter
* [Atom](README.md#ref_atom)

**Test type**:

Automated

**Notes**

[1] Is the hreflang attribute mandatory if data in only 1 language is provided? If so, this ATS is not automatically testable and the ATS should be removed.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
link <a name="downloadlink"></a> | //atom:entry/atom:link[(@rel='alternate' and @type!='application/atom+xml' and number(@length) > 0) or (@rel='section')]
hreflang <a name="hreflang"></a> | //atom:link[@rel=('alternate','section')]/@hreflang
