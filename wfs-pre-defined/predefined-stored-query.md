# Predefined Stored Query

**Purpose**:
Pre-defined Stored Queries must be provided to make pre-defined datasets available. Any possible (i.e. available) combinations of CRS/DataSetIdCode/DataSetIdNamespace/language must be made available through pre-defined stored queries. Pre-defined Stored Queries must use the parameter names 'CRS', 'DataSetIdCode', 'DataSetIdNamespace' and 'Language' to identify the CRS, dataset ID code, dataset ID namespace and language components of a query.

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/extended-capabilities)

**Test method**

* Perform a DescribeStoredQueries-request. Test that the [DescribeStoredQueriesResponse](#DescribeStoredQueriesResponse) contains at least one [StoredQueryDescription](#StoredQueryDescription) with the [Parameters](#Parameter): '[CRS](#CRS)', '[DataSetIdCode](#DataSetIdCode)', '[DataSetIdNamespace](#DataSetIdNamespace)' and '[Language](#Language)'.
* Perform a GetCapabilities request and collect all combinations of: [supported CRS](#supportedCRS), [supported language](#supportedLanguage), [SpatialDataSetIdentifier ID code](#SpatialDataSetIdentifierCode) and [SpatialDataSetIdentifier Namespace](#SpatialDataSetIdentifierNamespace)
* For each combination of [supported CRS](#supportedCRS), [supported language](#supportedLanguage), [SpatialDataSetIdentifier ID code](#SpatialDataSetIdentifierCode) and [SpatialDataSetIdentifier Namespace](#SpatialDataSetIdentifierNamespace): perform a GetFeature request with the [Stored Query ID](#storedQueryId) from the [DescribeStoredQueriesResponse](#DescribeStoredQueriesResponse) as defined in the first step. The parameter values in this request are defined as: [CRS](#CRS) is [supported CRS](#supportedCRS), [Language](#Language) is [supported language](#supportedLanguage), [DataSetIdCode](#DataSetIdCode) is [SpatialDataSetIdentifier ID code](#SpatialDataSetIdentifierCode) and [DataSetIdNamespace](#DataSetIdNamespace) is [SpatialDataSetIdentifier Namespace](#SpatialDataSetIdentifierNamespace). The response of the GetFeature request with the [Stored Query ID](#storedQueryId) must contain a wfs:FeatureCollection in the requested CRS.


**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#ref_TG_DL), Requirements 49, 50, 51

**Test type**:

Automated

**Notes**

TG Requirements 49, 50 and 51 together specify the use of Stored Queries to make pre-defined datasets available.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-service/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DescribeStoredQueriesResponse <a name="DescribeStoredQueriesResponse"></a> | /wfs:DescribeStoredQueriesResponse
StoredQueryDescription <a name="StoredQueryDescription"></a>| /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription
Parameter <a name="Parameter"></a>| /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter
CRS <a name="CRS"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='CRS']
DataSetIdCode <a name="DataSetIdCode"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='DataSetIdCode']
DataSetIdNamespace <a name="DataSetIdNamespace"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='DataSetIdNamespace']
Language <a name="Language"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='Language']
Stored Query ID <a name="storedQueryId"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/@id
supported CRS <a name="supportedCRS"></a> | //wfs:DefaultCRS combined with //wfs:OtherCRS
supported language <a name="supportedLanguage"></a> | //inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
SpatialDataSetIdentifier ID code <a name="SpatialDataSetIdentifierCode"></a> | //inspire_dls:ExtendedCapabilities/inspire_dls:SpatialDataSetIdentifier/inspire_common:Code
SpatialDataSetIdentifier Namespace <a name="SpatialDataSetIdentifierNamespace"></a>| //inspire_dls:ExtendedCapabilities/inspire_dls:SpatialDataSetIdentifier/inspire_common:Namespace
