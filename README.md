# OpenStreetMap import schema

This XML schema is intended for prepairing outside elements to be imported to OpenStreetMap data.

## The goal

The goal of this schema is to have a standard schema for importing data to OpenStreetMap. This schema could then be used by various import or comparison tools. This would then make it easier to publish those XML files which could be analysed and scrutinised by the community before any import goes through.

## XML Elements

### Domain

Domain is used to give us a strict subset of data from OpenStreetMap that is the domain of this import. If all elements of this import have a unique tag `ref:HR:e-matica=*` which isn't used anywhere else, than the domain can only reference that tag. If this import has all capital cities of the world, then domain should have tags `place=city` and `capital=yes`. 

### Types of importing elements

* poi - imported element can be whatever type
* node - must be a node
* way - must be a way
* relation - must be a relation
* area - must be a closed way or a multipolygon
* waychain - must be a chain of ways that connect to each other with their ending nodes
* ...

### Tags

Each of those elements can have tags entered.

## Examples

```
<osm source="http://opendata.com/e-school-data">
  <domain>
    <tag k="ref:HR:e-school-data" />
  </domain>
  <poi>
    <tag k="name" v="Osnovna škola Centar" function="match" />
    <tag k="operator:type" v="public" function="match" />
    <tag k="phone" v="+385 91 48 55 095" function="comparePhoneNumber" />

  </poi>
  <poi>
    <tag k="name" v="Osnovna škola Ivana Gundulića" function="match" />
    <tag k="operator:type" v="public" function="match" />

  </poi>
</osm>
```
