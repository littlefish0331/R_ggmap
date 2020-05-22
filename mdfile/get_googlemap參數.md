# get_googlemap參數

Get a Google Map.  
把說明文件中，列出我覺得實用且重要的。  
記得要開啟 Google maps api 的 statci map 和 Geocode 功能。

- center:  
the center of the map; either a longitude/latitude numeric vector or a string containing a location, in which case geocode is called with source = "google".(default: c(lon = -95.3632715, lat = 29.7632836), houston, texas)  

- zoom:  
map zoom; an integer from 3 (continent 大陸) to 21 (building), default value 10 (city)

- size:  
rectangular dimensions of map in pixels - horizontal x vertical - with a max of c(640, 640). this parameter is affected in a multiplicative way by scale.  
地圖的矩形尺寸(以像素為單位-水平x垂直-最大值為c(640，640)。此受參數scale影響成倍數。

- scale:  
multiplicative factor for the number of pixels returned possible values are 1, 2, or 4 (e.g. size = c(640,640) and scale = 2 returns an image with 1280x1280 pixels). 4 is reserved for google business users only. scale also affects the size of labels as well.  
返回的像素數的乘數可能是1、2或4(例如size = c(640,640)，而scale = 2將返回1280x1280像素的圖像)。4只保留給google業務用戶。scale也會影響labels的大小。

- format:  
character string providing image format - png, jpeg, and gif formats available in various flavors.

- maptype:  
character string providing google map theme. options available are "terrain", "satellite", "roadmap", and "hybrid"。  
地形, 衛星, 路線圖, 路線+地形。

- language:  
character string providing language of map labels (for themes with them) in the format "en-EN". not all languages are supported; for those which aren't the default language is used。  
預設 en-EN，可以改用 zh-TW. zh-CN

- messaging:  
turn messaging on/off

- urlonly:  
return url only

- filename:  
destination file for download (file extension added according to format). Default NULL means a random tempfile.  
ggmap會下載查詢的圖檔到暫存的資料夾，當之後查詢同樣的東西時，可以減少負擔。

- color:  
color or black-and-white.  
參數可填入 bw, color

- force:  
if the map is on file, should a new map be looked up?  
已經查過的區域圖塊，還要再重新找查嗎?

- where:  
where should the file drawer be located (without terminating "/")  
這個功能其實我沒有很懂。

- archiving:  
use archived maps. note: by changing to TRUE you agree to the one of the approved uses listed in the Google Maps API Terms of Service : http://developers.google.com/maps/terms.  
使用存檔的地圖。 注意：更改為TRUE，即表示您同意Google Maps API服務條款。

- ext:  
domain extension (e.g. "com", "co.nz")

- inject:  
character string to add to the url

- region:  
borders to display as a region code specified as a two-character ccTLD ("top-level domain") value, see http://en.wikipedia.org/wiki/List_of_Internet_top-level_domains#Country_code_top-level_domains.  
可以填入tw。

- markers:  
data.frame with first column longitude, second column latitude, for which google markers should be embedded in the map image, or character string to be passed directly to api.  
點位資料表 [longitude, latitude]

- path:  
data.frame (or list of data.frames) with first column longitude, second column latitude, for which a single path should be embedded in the map image, or character string to be passed directly to api.  
路徑資料表 [longitude, latitude]

- visible:  
a location as a longitude/latitude numeric vector (or data frame with first column longitude, second latitude) or vector of character string addresses which should be visible in map extent.

- style:  
character string to be supplied directly to the api for the style argument or a named vector (see examples). this is a powerful complex specification, see https://developers.google.com/maps/documentation/staticmaps/
