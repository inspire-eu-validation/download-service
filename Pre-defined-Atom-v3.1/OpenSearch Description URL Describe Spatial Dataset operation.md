# OpenSearch Description URL Describe Spatial Dataset operation

**Purpose**:

The OpenSearch description must contain a ["Url" element](#urlelement) that describes a template URL for the Describe Spatial Data Set operation. This template must accept the INSPIRE parameters "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and the OpenSearch "language" parameter. The ["Url" element](#urlelement) must have an attribute "type" with a value of "application/atom+xml" and an attribute "rel" with the value "describedby".

**Test method**

* test if the OpenSearch Description provides a [Describe Spatial Dataset url](#describespatialdataseturl)
* for this [Describe Spatial Dataset url](#describespatialdataseturl), fill in the parameters for "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and "language" and resolve the [Describe Spatial Dataset url](#describespatialdataseturl) and test if it provides a document with the HTTP Header Content-Type "application/atom+xml"

**Reference(s)**:

* [TG DL](README.md#ref_TG_DL), Req 42
* [OpenSearch](README.md#ref_opensearch)

**Test type**:

Automated

**Notes**

[1] The values for the parameters "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and "language" can be obtained from the OpenSearch description

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
url element <a name="urlelement"></a> | /os:OpenSearchDescription/os:Url
Describe Spatial Dataset url <a name="describespatialdataseturl"></a> | /os:OpenSearchDescription/os:Url[@rel='describedby' and @type='application/atom+xml' and starts-with(@template,'http') and contains(@template,'spatial_dataset_identifier_code') and contains(@template,'spatial_dataset_identifier_namespace') and contains(@template,'language')]
