# get_openstreetmap

Get an OpenStreetMap.
把說明文件中，列出我覺得實用且重要的。  
現在 ggmap 無法 呼叫到 OpenStreetMap 的圖層做使用，  
it seems that OpenStreetMap has blocked external applications (such as ggmap) from calling its export API function because of the load this puts on the OSM servers.  

所以如果想用 OpenStreat Map，請改用其他 papckage。  
比如: OpenStreetMap, rosm

## 參數說明

- bbox:  
a bounding box in the format c(lowerleftlon, lowerleftlat, upperrightlon, upperrightlat)

- scale:  
scale parameter, see http://wiki.openstreetmap.org/wiki/MinScaleDenominator. smaller scales provide a finer degree of detail, where larger scales produce more coarse detail.  
**比例參數，請參見http://wiki.openstreetmap.org/wiki/MinScaleDenominator。 較小的比例會提供更好的細節程度，而較大的比例會產生更粗糙的細節。**  
The scale argument is a tricky number to correctly specify. In most cases, if you get an error when downloading an openstreetmap the error is attributable to an improper scale specification.  
**scale參數是一個難以正確指定的棘手數字。 在大多數情況下，如果在下載openstreetmap時遇到錯誤，則該錯誤可歸因於比例尺規格不正確。**  
OSM_scale_lookup can help; but the best way to get in the correct range is to go to http://www.openstreetmap.org/, navigate to the map of interest, click export at the top of the page, click 'map image' and then copy down the scale listed.  
**OSM_scale_lookup可以提供幫助； 但是進入正確範圍的最佳方法是轉到http://www.openstreetmap.org/，導航至感興趣的地圖，單擊頁面頂部的導出，單擊“地圖圖像”，然後向下複製 列出的比例。**

- format:  
character string providing image format - png, jpeg, svg, pdf, and ps formats

- messaging:  
turn messaging on/off

- urlonly:  
return url only

- filename:  
destination file for download (file extension added according to format). Default NULL means a random tempfile.

- color:  
color or black-and-white
