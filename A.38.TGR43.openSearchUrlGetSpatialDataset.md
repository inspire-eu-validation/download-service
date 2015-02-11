# OpenSearch Description provides at least one URL for Get Spatial Dataset operation

**Purpose**: 

The OpenSearch description must contain a ["Url" element](#urlelement) that describes a template URL for the Get Spatial Data Set operation. This template must accept the INSPIRE parameters "crs", "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and the OpenSearch "language" parameter. The ["Url" element](#urlelement) must have an attribute "type" with a value corresponding to the media type of the result and an attribute "rel" with the value "results".

**Test method**

* test if the OpenSearch Description provides at least one [Get Spatial Dataset url](#getspatialdataseturl) 
* for each [Get Spatial Dataset url](#getspatialdataseturl), fill in the parameters for "crs", "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and "language" and resolve the [Get Spatial Dataset url](#getspatialdataseturl) 
* test if the HTTP response of the previous step has the same content-type as the [media-type](#mediatype) of the [Get Spatial Dataset url](#getspatialdataseturl)

**Reference(s)**: 

* IR section 3 (3.1-3.2.1)
* TG, Req 43
* [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Test type**: 

Automated

**Notes**

[1] The values for the parameters "crs", "spatial_dataset_identifier_code", "spatial_dataset_identifier_namespace" and "language" can be obtained from the OpenSearch description

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
url element <a name="urlelement"></a> | /os:OpenSearchDescription/os:Url
Get Spatial Dataset url <a name="getspatialdataseturl"></a> | /os:OpenSearchDescription/os:Url[@rel='results' and starts-with(@template,'http') and contains(@template,'crs') and contains(@template,'spatial_dataset_identifier_code') and contains(@template,'spatial_dataset_identifier_namespace') and contains(@template,'language')]
media-type <a name="mediatype"></a> | /os:OpenSearchDescription/os:Url/@type