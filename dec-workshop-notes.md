# Raw notes from the MD & NS validation workshop

## Requirement 1

Ensure uniqueness of each of the top-level feed spatial_dataset_identifier_code and spatial_dataset_identifier_namespace combination.

## Requirement 2

All Atom feed must validate against the RFC 4287.

## Requirement 3

All Atom feed must validate against the GeoRSS-Simple subset GeoRSS language, as specified in schema version 1.1 

## Requirement 4

All OpenSearch documents referred to in Atom feeds must conform to the OpenSearch version 1.1 spec document.
There is no official XML schema however. So the ETS needs to implement the test based on the schema document directly.

## Requirement 5

title must be non-empty text as in the test for MD titles: text content must include at least one alpha-numeric letter

## Requirement 6

The attribute rel with value "describedby" and type with value "application/xml" must be exist.

link href attribute must be there and the link must resolve to a service MD record. Same principle logic for validation 
than with WMS: the URL in the href attribute must resolve to a valid XML document with
   a valid gmd:MD_Metadata element as the root element. This MD_Metadata element must describe an INSPIRE Download Service
   (according the the MD tests), and it's distributionInfo/\*/transferOptions/\*/onLine/\*/linkage must contain
   a URL reference to an Atom Download Service Feed document. This URL needs to be resolved in
   order to check that it returns an Atom Download Service Feed document with the "describedby" rel link pointing to the same address than the one in the Download Service Feed under validation. Note that the URLs used for fetching the Atom documents, or the contents of the Download Service Feed documents do not have to match. Note 2: the INSPIRE language request parameters in the compared metadata record URLs must be ignored in the comparison.

## Requirement 7

hreflang value must be the same as the xml:lang attribute of the Atom feed, and if that is not given 
it must the default language code defined in the OpenSearch description.

## Requirement 8

Is the hreflang necessary here?
Recommendation to the TG editors to remove the hreflnag attr from the req text

## Requirement 16

Not testable unless the rel + type mentioned here is taken as an indicator of a "hybrid" service

## Requirement 26

Test that the URL resolves to a file. The final result or resolving the URL (after possible server redirections with 301 or 302 status codes and possible authentication) must be an HTTP response with status code 200 and content length bigger than 0



