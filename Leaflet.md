# University of IOWA
Wen Che  
August 17, 2017  



## Leaflet

I tried to map out certain University of Iowa campus locations around Iowa city. First I created multiple markers with data frame with columns of lat and lng for latitude and longitude.I also customized text pop ups with valid URL which appears when you click on the marker.


```r
library(leaflet)
```

```
## Warning: package 'leaflet' was built under R version 3.3.3
```

```r
iowaLatLong <- data.frame(
  lat = c(41.664468, 41.657515, 41.660094, 41.664326),
  lng = c(-91.542444, -91.542787, -91.536867, -91.535773))
iowaSites<-c(
  "<a href='https://www.public-health.uiowa.edu/biostat/'>College of Public Health</a>",
  "<a href='https://law.uiowa.edu/'>College of Law</a>",
  "<a href='https://www.engineering.uiowa.edu/'>College of Engineering</a>",
  "<a href='https://admissions.uiowa.edu/visit-campus/'>Admission Vistor Center</a>"
  )
iowaLatLong %>% 
  leaflet() %>%
  addTiles() %>%
  addMarkers(popup = iowaSites) %>%
  addCircleMarkers()
```

<!--html_preserve--><div id="htmlwidget-27d8c358e920675b622c" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-27d8c358e920675b622c">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"maxNativeZoom":null,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"continuousWorld":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap\u003c/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA\u003c/a>"}]},{"method":"addMarkers","args":[[41.664468,41.657515,41.660094,41.664326],[-91.542444,-91.542787,-91.536867,-91.535773],null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},["<a href='https://www.public-health.uiowa.edu/biostat/'>College of Public Health\u003c/a>","<a href='https://law.uiowa.edu/'>College of Law\u003c/a>","<a href='https://www.engineering.uiowa.edu/'>College of Engineering\u003c/a>","<a href='https://admissions.uiowa.edu/visit-campus/'>Admission Vistor Center\u003c/a>"],null,null,null,null,null,null]},{"method":"addCircleMarkers","args":[[41.664468,41.657515,41.660094,41.664326],[-91.542444,-91.542787,-91.536867,-91.535773],10,null,null,{"lineCap":null,"lineJoin":null,"clickable":true,"pointerEvents":null,"className":"","stroke":true,"color":"#03F","weight":5,"opacity":0.5,"fill":true,"fillColor":"#03F","fillOpacity":0.2,"dashArray":null},null,null,null,null,null,null,null]}],"limits":{"lat":[41.657515,41.664468],"lng":[-91.542787,-91.535773]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

