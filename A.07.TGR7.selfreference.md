# Download Service feed contains a self-reference link

**Purpose**:

The Download Service feed must provide a self-reference link. This link must be a HTTP URI that resolves to the Download Service feed document. The value of the 'rel' attribute of this element shall be 'self', the 'hreflang' attribute shall use the appropriate language code and the value of the 'type' attribute shall be 'application/atom+xml'.

**Test method**

* check existence of the [self link](#selflink)
* the [self link](#selflink) must be the same as the Download Service feed URI
* the [self link](#selflink)'s [hreflang attribute](#hreflang) must be the same as the [xml:lang attribute](#xmllang) of the Atom feed or if the [xml:lang attribute](#xmllang) is not given, it must be the default language code defined in the OpenSearch description.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 7
* [Atom](README.md#ref_atom)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
self link <a name="selflink"></a> | /atom:feed/atom:link[@rel='self' and @type='application/atom+xml']/@href
hreflang attribute <a name="hreflang"></a> | /atom:feed/atom:link[@rel='self' and @type='application/atom+xml']/@hreflang
xml:lang attribute <a name="xmllang"></a> | /atom:feed/atom:title/@xml:lang
