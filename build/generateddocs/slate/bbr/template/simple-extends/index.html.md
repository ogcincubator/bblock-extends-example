---
title: Simple extends (Schema)

language_tabs:
  - shell
  - python: Python
  - javascript: Javascript

toc_footers:
  - Version 0.1
  - <a href='#'>Simple extends</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Simple extends (Schema)
---


# Simple extends `ogc.bbr.template.simple-extends`

This Building Block shows how to use the extension mechanism

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>

# Description

## Qui hastarum tectus Cithaeron iuvabat

Lorem markdownum vestigia sanguine rursus undis, suspenderat meo mox conlegerat
temperat sucos. Est graves dant sentire sanguinis flores respondent testari.

> Videri vias quid Ausoniae sua flores ante, reminiscitur fuit est. Semel
> [hectora](http://silvaque.org/) peregrinaeque rudem exercent in, Troiana si
> Asida instabilesque somno sed.

## Iam vota cui dilataque peterem

Tinxit lumina lacer liquidarum Aiax si mergitur sed fueris capitisque **et
cadit** contigerant rectum [ferar](http://prosternit.com/quoque.html) temperat.
Monet caput adsensere Ityn furentibus gelidos.
# Examples

## This is an example with just a description and no code snippets.

This is the content of the example.

In **Markdown** format.


## Examples can have content and/or code snippets.

The content of this example. 

```shell
echo 'Hello, world!'
```

```python
print('Hello, world!')
```

```javascript
console.log('Hello, world!')
```


# JSON Schema

```yaml--schema
$schema: https://json-schema.org/draft/2020-12/schema
allOf:
- $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/feature/schema.yaml
- description: Schema for my building block
  x-jsonld-context: context.jsonld
  type: object
  properties:
    a:
      type: string
      format: uri
      x-jsonld-id: https://example.org/my-bb-model/a
      x-jsonld-type: '@id'
    b:
      type: number
      x-jsonld-id: https://example.org/my-bb-model/b
  required:
  - a
  - b

```

Links to the schema:

* YAML version: <a href="https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/schema.yaml" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/schema.yaml</a>
* JSON version: <a href="https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/schema.json" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "type": "@type",
    "id": "@id",
    "properties": "geojson:properties",
    "geometry": {
      "@id": "geojson:geometry",
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        }
      }
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "links": {
      "@id": "rdfs:seeAlso",
      "@context": {
        "href": "@id",
        "title": "rdfs:label"
      }
    },
    "a": {
      "@id": "https://example.org/my-bb-model/a",
      "@type": "@id"
    },
    "b": "https://example.org/my-bb-model/b",
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#"
  }
}
```

You can find the full JSON-LD context here:
<a href="https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/context.jsonld" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblock-extends-example/master/build/annotated/bbr/template/simple-extends/context.jsonld</a>

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblock-extends-example" target="_blank">https://github.com/ogcincubator/bblock-extends-example</a>
* Path: `_sources/simple-extends`

