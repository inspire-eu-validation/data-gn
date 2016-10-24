# Conformance class: GML application schemas, Geographical Names (DRAFT)

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Geographical Names'. This conformance class examines the data set against requirements associated with the GML application schema. Both currently approved GML application schema versions (3.0 and 4.0) are tested.

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Geographical Names](http://inspire.ec.europa.eu/id/ats/data-gn/3.1).

## Standardization target type

INSPIRE spatial data set encoded in GML, Geographical Names features

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-GN <a name="ref_TG_DS_GN"></a>   | [INSPIRE Data Specification on Geographical Names – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_GN_v3.1.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-GN](#ref_TG_DS_GN)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Basic test](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-gml/basic)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gn          | http://inspire.ec.europa.eu/schemas/gn/4.0 or urn:x-inspire:specification:gmlas:GeographicalNames:3.0
