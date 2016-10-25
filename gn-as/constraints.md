# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* At least one of the two attributes pronunciationSoundLink and pronunciationIPA shall not be void; OCL: "inv: self.pronounciationIPA -> notEmpty() or self.pronounciationSoundLink -> notEmpty()" Verify that for all features either or both [pronunciationSoundLink](#pronunciationSoundLink) or [pronunciationIPA](#pronunciationIPA) is not void.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-gn/3.2/gn-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-gn/3.2/gn-as/README#ref_TG_DS_PS)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-gn/3.2/gn-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
pronunciationSoundLink <a name="pronunciationSoundLink"></a> 	|  //schema-element(gn:NamedPlace)/gn:PronunciationOfName/gn:pronunciationSoundLink
pronunciationIPA <a name="pronunciationIPA"></a> 	| 	//schema-element(gn:NamedPlace)/gn:PronunciationOfName/gn:pronunciationIPA