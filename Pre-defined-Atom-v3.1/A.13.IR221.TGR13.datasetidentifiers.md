# Download Service feed contains dataset identifiers

**Purpose**:

The Download Service feed must provide the INSPIRE identifier elements [dataset identifier code](#datasetidentifiercode) and [dataset identifier namespace](#datasetidentifiernamespace) for each dataset

 **Test method**

* resolve the [describedby link](#describedbylink) to get the metadata document of the service

For each [entry](#entry):
* the [dataset identifier code](#datasetidentifiercode) and [dataset identifier namespace](#datasetidentifiernamespace) must be non-empty text elements; the text content of both elements must include at least one alpha-numeric letter.

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 13
* [IR NS](README.md#ref_IR_NS), section 2.2.1, Discovery Service Metadata parameter

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
describedby link <a name="describedbylink"></a> | /atom:feed/atom:link[@rel='describedby' and (@type='application/xml' or @type='application/vnd.ogc.csw.GetRecordByIdResponse_xml')]/@href
entry <a name="entry"></a> | //atom:entry
dataset identifier code <a name="datasetidentifiercode"></a> | //atom:entry/inspire_dls:spatial_dataset_identifier_code
dataset identifier namespace <a name="datasetidentifiernamespace"></a> | //atom:entry/inspire_dls:spatial_dataset_identifier_namespace
