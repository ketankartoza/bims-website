# Cartography

GeoServer provides a couple of ways to symbolize vector and raster data. The most
common way is by using SLD(styled layer descriptor) which is an OGC standard.
GeoServer also adds some flavour to the format which enriches how to symbolize vector/raster
data. Other less common ways to symbolize data include using CSS(Cascading style sheets) and YSLD.

There are various open source software which allows you to export SLD natively. Since we are
familiar with QGIS we will use it as our defacto Desktop GIS system. 

**Note:** Although QGIS can export SLD it does not produce a 1-1 mapping of the rich
cartography that is available in QGIS. It is recommended to use simple styles when your goal
is to use the SLD exporter from QGIS.

## Styling Vector layers in QGIS

1) Load your vector layers in QGIS.
2) Right-click on the vector layer and choose the symbology tab.
    ![symbology.png](img/symbology-tab.png)
3) Select an appropriate style from the options. Be thoughtful of all the 
cartographic rules and the limitations of the exporter when choosing a style.
4) If you are satisfied with your result click **Apply**.
5) Click on the **Style** link to show the hidden context menu.
    ![style-layer.png](img/save-style.png)
6) Save your style as SLD.
    ![save-sld.png](img/save-style-sld.png)
7) Export the SLD to disk and wait to upload to GeoServer.

## Publishing style in GeoServer

1) Navigate to GeoServer and click on the style tab.
2) Click to **Add New Style**.
3) Browse and upload your style into GeoServer.
    ![upload-style.png](img/upload-style.png)
4) Submit your results and this will take you back to your style. 
5) Use the search box at the top of the style to identify the name of the style you created above.
    ![search-style.png](img/search-style.png)
6) Open the style again and indicated below.
    ![open-style-tab-again.png](img/style-tab-opening.png)
7) Select the layer you want to associate your style with. 
    ![associated-style.png](img/association-style.png)
    There are two options 
    * Default style - Visible when you preview the map.
    * Associated style - Visible when you change the URL for a GetMap / Getlegend request
8) Submit your results.

**Note:** This process applies to also styling raster data.