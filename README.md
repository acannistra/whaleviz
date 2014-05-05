# Whale Viz
> A project to visualize whale sightings off the coast of California (and to learn [D3](http://www.d3js.org))

## Converting Whale Files
Performed

    ogr2ogr -f GeoJSON  -t_srs EPSG:4326 <whale>.json <whale>.shp &&
    topojson -p -o <whale>.topojson <whale>.json

for all whale shapefiles. Then, to combine whales and state outline:

    topojson -o combined.json tl_2014_us_state/us_states.topojson <whale1>/<whale1>.topojson <whale2>/<whale2>.topojson ...