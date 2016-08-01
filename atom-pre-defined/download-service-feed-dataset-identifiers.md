# Download Service feed dataset identifiers

**Purpose**: The Download Service feed must provide the INSPIRE identifier elements [dataset identifier code](#datasetidentifiercode) and [dataset identifier namespace](#datasetidentifiernamespace) for each dataset

**Prerequisites**

**Test method**

For each [entry](#entry):

* The [dataset identifier code](#datasetidentifiercode) and [dataset identifier namespace](#datasetidentifiernamespace) must be non-empty text elements; the text content of both elements must include at least one alpha-numeric character.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#ref_TG_DL), Requirement 13

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/atom-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
entry <a name="entry"></a> | //atom:entry
dataset identifier code <a name="datasetidentifiercode"></a> | //atom:entry/inspire_dls:spatial_dataset_identifier_code
dataset identifier namespace <a name="datasetidentifiernamespace"></a> | //atom:entry/inspire_dls:spatial_dataset_identifier_namespace
