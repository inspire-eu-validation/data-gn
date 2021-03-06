# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Geographical Names application schema, the following properties have to be tested:
* [NamedPlaceType (v3)](#NamedPlaceType3). Valid values:
  * administrativeUnit
  * building
  * hydrography
  * landcover
  * landform
  * populatedPlace
  * protectedSite
  * transportNetwork
  * other
* [NamedPlaceType (v4)](#NamedPlaceType4). Valid values:
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/administrativeUnit
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/building
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/hydrography
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/landcover
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/landform
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/other
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/populatedPlace
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/protectedSite
  * http://inspire.ec.europa.eu/codelist/NamedPlaceTypeValue/transportNetwork
  
Other code list values are part of the GeographicalName data type and are therefore part of the Abstract Test Suite [Schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas).

The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.1/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
NamedPlaceType (v3) <a name="NamedPlaceType3"></a>   | //schema-element(gn3:NamedPlace)@type
NamedPlaceType (v4) <a name="NamedPlaceType4"></a>   | //schema-element(gn:NamedPlace)@type
