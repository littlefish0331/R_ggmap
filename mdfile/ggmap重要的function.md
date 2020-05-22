# ggmap重要的function

- osm無法使用了!!
- get_map(): 取得map資料後，再用ggmap()繪製出來。
  - extent: how much of the plot should the map take up? "normal, device", or "panel" (default)

**繪製地圖:**

兩個很像，但是傳入的參數不太一樣。  

- qmap: 參數比較少(我覺得啦~)，是用來繪製地圖的。  
- qmplot: 參數比較多(我覺得啦~)，是用來繪製地圖外，再加上data的。

但大致上差不多。

- qmap(): qmap is a wrapper for ggmap and get_map.
  - location: 會需要 google map geocode api
  - c(left, bottom, right, top): stamen, 

- qmplot(): Quick map plot. qmplot is the ggmap equivalent to the ggplot2 function qplot and allows for the quick plotting of maps with data/models/etc.

  
  