# OpenSearch Description provides Query examples for each dataset

**Purpose**:

For each dataset available the OpenSearch description must contain a ["Query" element](#queryelement)" element that has a "role" attribute with the value "example" and "spatial_dataset_identifier_code" and "spatial_dataset_identifier_namespace" attributes together containing unique spatial dataset identifier. The value of the "crs" and "language" attributes must be set to the values considered as the default ones by the service provider.

**Test method**

* test if there is at least one ["Query" element](#queryelement)

For each ["Query" element](#queryelement):
* create a [Describe Spatial Dataset url](#describespatialdataseturl) with the values of the provided inspire_dls:spatial_dataset_identifier_code and inspire_dls:spatial_dataset_identifier_namespace from the ["Query" element](#queryelement)
* resolve that [Describe Spatial Dataset url](#describespatialdataseturl)
* test if the response is an Atom feed containing at least one [category CRS](#categorycrs)
* For each [category CRS](#categorycrs), create a [Get Spatial Dataset url](#getspatialdataseturl) with the CRS, the provided inspire_dls:spatial_dataset_identifier_code and inspire_dls:spatial_dataset_identifier_namespace
* resolve the [Get Spatial Dataset url](#getspatialdataseturl)
* check the HTTP response code to be a valid code from: 200,206,301,303,303

**Reference(s)**:

* [IR NS](README.md#ref_IR_NS), M1, section 3 (3.1-3.2.1), 4 (4.1-4.2.1)
* [TG DL](README.md#ref_TG_DL), Req 44
* [OpenSearch 1.1 specification](http://www.opensearch.org/Specifications/OpenSearch/1.1)

**Test type**:

Automated

**Notes**

[1] Are the "crs" and "language" attributes mandatory? This is not clear from the requirement, but would make sense and is assumed to be so.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Query element <a name="queryelement"></a> | /os:OpenSearchDescription/os:Query[@role='example' and string-length(@inspire_dls:spatial_dataset_identifier_code) > 0 and string-length(@inspire_dls:spatial_dataset_identifier_namespace) > 0 ]
Describe Spatial Dataset url <a name="describespatialdataseturl"></a> | /os:OpenSearchDescription/os:Url[@rel='describedby' and @type='application/atom+xml' and starts-with(@template,'http') and contains(@template,'spatial_dataset_identifier_code') and contains(@template,'spatial_dataset_identifier_namespace') and contains(@template,'language')]
Get Spatial Dataset url <a name="getspatialdataseturl"></a> | /os:OpenSearchDescription/os:Url[@rel='results' and starts-with(@template,'http') and contains(@template,'crs') and contains(@template,'spatial_dataset_identifier_code') and contains(@template,'spatial_dataset_identifier_namespace') and contains(@template,'language')]
category CRS <a name="categorycrs"></a> | //atom:entry/atom:category[string-length(@term) > 0]
