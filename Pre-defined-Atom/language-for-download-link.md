# Language for download link

**Purpose**:

Where alternative language representations of datasets are linked to, the \" [hreflang attribute](#hreflang) \" attribute of the [link](#downloadlink) element must be used to indicate the language of the target dataset as described in the Atom specification.

**Test method**

* if an [entry](#entry) has more than 1 download [link](#downloadlink), test that each of these download links provides the [hreflang attribute](#hreflang)

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 31
* [Atom](README.md#ref_atom)

**Test type**:

Automated

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry/
link <a name="downloadlink"></a> | //atom:entry/atom:link[(@rel='alternate' and @type!='application/atom+xml' and number(@length) > 0) or (@rel='section')]
hreflang <a name="hreflang"></a> | //atom:link[@rel=('alternate','section')]/@hreflang
