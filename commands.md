## Commands for Overpass Turbo

These are the commands used to read data from OSM

### Knoxville District K&A Line - NS

```javascript
[out:json];
area["ISO3166-2"="US-TN"][admin_level=4];
way["name"="Knoxville District K&A Line"]["railway"="rail"](area);
out meta;/*fixed by auto repair*/
>;
out meta qt;
```

### KD Subdivision - CSV

Blount County

```javascript
[out:json];
area["nist:fips_code"="47009"];
way["name"="KD Subdivision"]["tiger:county"~"^Blount"]["railway"="rail"](area);
out meta;/*fixed by auto repair*/
>;
out meta qt;/*fixed by auto repair*/
```

Knox County (south of Middlebrook Pike)

```javascript
[out:json];
area["ISO3166-2"="US-TN"][admin_level=4];
way["name"="KD Subdivision"]["tiger:county"~"^Knox"]["railway"="rail"](area); /*["tiger:county"~"^Blount"]*/
out meta;/*fixed by auto repair*/
>;
out meta qt;/*fixed by auto repair*/
```
