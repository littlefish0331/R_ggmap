# get_stamenmap

Get a Stamen Map.  
把說明文件中，列出我覺得實用且重要的。  

get_stamenmap accesses a tile server for Stamen Maps and downloads/stitches map tiles/formats a map image.  
**Note that Stamen maps don't cover the entire world.**

- bbox:  
a bounding box in the format c(lowerleftlon, lowerleftlat, upperrightlon, upperrightlat).

- zoom:  
a zoom level

- maptype:  
terrain, terrain-background, terrain-labels, terrain-lines, toner, toner-2010, toner-2011, toner-background, toner-hybrid, toner-labels, toner-lines, toner-lite, or watercolor.  
地形，地形背景，地形標籤，地形線，碳粉，碳粉2010，碳粉2011，碳粉背景，碳粉混合，碳粉標籤，碳粉線，碳粉精或水彩。

- crop:  
crop raw map tiles to specified bounding box. if FALSE, the resulting map will more than cover the bounding box specified.  
將原始地圖圖塊裁剪到指定的邊界框。 如果為FALSE，則生成的地圖將覆蓋指定的邊界框。

- messaging:  
turn messaging on/off

- urlonly:  
return url only

- color:  
color or black-and-white (use force = TRUE if you've already downloaded the images)

- force:  
if the map is on file, should a new map be looked up?

- where:  
where should the file drawer be located (without terminating "/")
