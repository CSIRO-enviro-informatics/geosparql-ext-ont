# GeoSPARQL Extensions Ontology
Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE)


## Metadata
* **IRI**
  * `http://linked.data.gov.au/def/geox`
* **Publisher(s)**
  * <a href='http://catalogue.linked.data.gov.au/org/csiro'>CSIRO</a>
* **Creators(s)**
  * <a href='https://orcid.org/0000-0002-3884-3420'>Simon J D Cox, CSIRO</a>
  * <a href='https://orcid.org/0000-0002-8742-7730'>Nicholas J Car, Surround Australia</a>
* **Created**
  * 2019-01-08
* **Modified**
  * 2020-02-04
* **Version Information**
  * Alpha version
* **Version IRI**
  * <a href="http://linked.data.gov.au/def/geox/1.1">http://linked.data.gov.au/def/geox/1.1</a>
* **Imports**
  * <a href="http://www.opengis.net/ont/geosparql">http://www.opengis.net/ont/geosparql</a>
  * <a href="http://linked.data.gov.au/def/datatype">http://linked.data.gov.au/def/datatype</a>
* **Ontology Source**
  * <a href="geox.ttl">RDF (turtle)</a>
* **Code Repository**
  * <https://github.com/CSIRO-enviro-informatics/geosparql-ext-ont>
### Description
<p>An extension to <a href="http://www.opengeospatial.org/standards/geosparql">GeoSPARQL</a> with new features for the representation of additional elements of feature geometry, such as spatial-resolution, length, area and volume. </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Namespaces](#namespaces)  


## Overview
![GeoSPARQL Extensions Ontology overview](./docs/geox.png)
**Figure 1:** Ontology overview  
## Classes
[Spatial measure](#Spatialmeasure),
### Spatial measure <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#SpatialMeasure`
Description | Spatial quantity computed or defined within a specified coordinate reference system
Super-classes |<a href="http://linked.data.gov.au/def/datatype/QuantitativeMeasure">data:QuantitativeMeasure</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#InCoordinateReferenceSystem">geox:inCRS</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1<br />
In domain of |<a href="#InCoordinateReferenceSystem">geox:inCRS</a><sup class="sup-op" title="object property">op</sup><br />
In range of |<a href="#haslength">geox:hasLength</a><sup class="sup-op" title="object property">op</sup><br /><a href="#hasarea">geox:hasArea</a><sup class="sup-op" title="object property">op</sup><br /><a href="#hasvolume">geox:hasVolume</a><sup class="sup-op" title="object property">op</sup><br />

## Object Properties
[has area](hasarea),
[has area in m2](hasareainm2),
[has length](haslength),
[has length in m](haslengthinm),
[has spatial resolution](hasspatialresolution),
[has spatial resolution in metres](hasspatialresolutioninmetres),
[has volume](hasvolume),
[has volume in m3](hasvolumeinm3),
[In Coordinate Reference System](InCoordinateReferenceSystem),
[is geometry of](isgeometryof),
[](hasarea)
### has area <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasArea`
Description | The area of a spatial object, expressed as a scaled number
Example | <pre>my:plot456<br />  :hasArea [<br />    data:uncertainty 0.5 ;<br />    data:unit &lt;http://qudt.org/vocab/unit/M2> ;<br />    data:value 63.9 ;<br />  ] ;<br />.</pre>
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#SpatialObject">geo:SpatialObject</a><sup class="sup-c" title="class">c</sup><br />
Range(s) |<a href="#Spatialmeasure">geox:SpatialMeasure</a><sup class="sup-c" title="class">c</sup><br />
[](hasareainm2)
### has area in m2 <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasAreaM2`
Description | The area of the spatial object in m^2
Example | <pre>my:plot456<br />  :hasAreaM2 [<br />    data:value 63.9 ;<br />  ] ;<br />.</pre>
Super-properties |<a href="#hasarea">geox:hasArea</a><sup class="sup-op" title="object property">op</sup><br />
[](haslength)
### has length <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasLength`
Description | The length of a spatial object, expressed as a scaled number
Example | <pre>my:road456<br />  :hasLength [<br />    data:uncertainty 5.0 ;<br />    data:unit &lt;http://qudt.org/vocab/unit/M> ;<br />    data:value 234.0 ;<br />  ] ;<br />.</pre>
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#SpatialObject">geo:SpatialObject</a><sup class="sup-c" title="class">c</sup><br />
Range(s) |<a href="#Spatialmeasure">geox:SpatialMeasure</a><sup class="sup-c" title="class">c</sup><br />
[](haslengthinm)
### has length in m <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasLengthM`
Description | The length of a spatial object in metres
Example | <pre>my:road456<br />  :hasLengthM [<br />    data:value 234.0 ;<br />  ] ;<br />.</pre>
Super-properties |<a href="#haslength">geox:hasLength</a><sup class="sup-op" title="object property">op</sup><br />
[](hasspatialresolution)
### has spatial resolution <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasResolution`
Description | The spatial resolution of the Geometry object, expressed as a linear measurement.
Example | <pre>my:image456<br />  :hasResolution [<br />    data:unit &lt;http://qudt.org/vocab/unit/M> ;<br />    data:value 30.0 ;<br />  ] ;<br />.</pre>
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#Geometry">geo:Geometry</a><sup class="sup-c" title="class">c</sup><br />
Range(s) |<a href="http://linked.data.gov.au/def/datatype/QuantitativeMeasure">data:QuantitativeMeasure</a><sup class="sup-c" title="class">c</sup><br />
[](hasspatialresolutioninmetres)
### has spatial resolution in metres <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasResolutionM`
Description | The spatial resolution of the Geometry object, expressed as a linear distance in metres
Example | <pre>my:image456<br />  :hasResolutionM [<br />    data:value 30.0 ;<br />  ] ;<br />.</pre>
Super-properties |<a href="#hasspatialresolution">geox:hasResolution</a><sup class="sup-op" title="object property">op</sup><br />
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#Geometry">geo:Geometry</a><sup class="sup-c" title="class">c</sup><br />
[](hasvolume)
### has volume <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasVolume`
Description | The volume of a spatial object, expressed as a scaled number
Example | <pre>my:swimmingPool99<br />  :hasVolume [<br />    data:unit &lt;http://qudt.org/vocab/unit/M3> ;<br />    data:value 3050.0 ;<br />  ] ;<br />.</pre>
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#SpatialObject">geo:SpatialObject</a><sup class="sup-c" title="class">c</sup><br />
Range(s) |<a href="#Spatialmeasure">geox:SpatialMeasure</a><sup class="sup-c" title="class">c</sup><br />
[](hasvolumeinm3)
### has volume in m3 <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#hasVolumeM3`
Description | The volume of a spatial object in cubic-metres
Example | <pre>my:swimmingPool99<br />  :hasVolumeM3 [<br />    data:value 3050.0 ;<br />  ] ;<br />.</pre>
Super-properties |<a href="#hasvolume">geox:hasVolume</a><sup class="sup-op" title="object property">op</sup><br />
[](InCoordinateReferenceSystem)
### In Coordinate Reference System <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#inCRS`
Description | The measure is defined or computed using this CRS. 
The CRS should be denoted by a URI Reference to a CRS definition, e.g. https://www.opengis.net/def/crs/EPSG/0/4326
Domain(s) |<a href="#Spatialmeasure">geox:SpatialMeasure</a><sup class="sup-c" title="class">c</sup><br />
[](isgeometryof)
### is geometry of <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/geox#isGeometryOf`
Description | link from a geometry object to the feature(s) for which it is a geometry
Domain(s) |<a href="http://www.opengis.net/ont/geosparql#Geometry">geo:Geometry</a><sup class="sup-c" title="class">c</sup><br />
Range(s) |<a href="http://www.opengis.net/ont/geosparql#Feature">geo:Feature</a><sup class="sup-c" title="class">c</sup><br />

## Namespaces
* **default (:)**
  * `http://linked.data.gov.au/def/geox#`
* **data**
  * `http://linked.data.gov.au/def/datatype/`
* **dc**
  * `http://purl.org/dc/elements/1.1/`
* **dcterms**
  * `http://purl.org/dc/terms/`
* **doap**
  * `http://usefulinc.com/ns/doap#`
* **geo**
  * `http://www.opengis.net/ont/geosparql#`
* **geox**
  * `http://linked.data.gov.au/def/geox#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `http://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **sosa**
  * `http://www.w3.org/ns/sosa/`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties :op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni
