# OpenStreetMap import schema

This XML schema is intended for mapping elements within outside data with OpenStreetMap data.

## Examples

```
<osm>
  <domain>
    <locationArea name="Croatia" />
    <tag k="amenity" v="school" />
    <tag k="ref:HR:e-matica" />
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
