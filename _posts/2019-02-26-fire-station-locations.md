
Metropolitan city relies on fire stations to provide safety and order specially during fire incidents.San Francisco City provides dataset of fire stations. However, they lack a map to illustrate their locations. To achieve this, I used `geopandas` for visualization. I extracted the coordinates of fire stations from another dataset and placed them on the map to identify each fire station. To test this, I compared the visualization with Google Maps. It seems that the visualization is somewhat similar on the map except for 3 stations that are far away.


```python
import pandas as pd
import geopandas as gpd
import matplotlib.pyplot as pl
from shapely.geometry import Point
import os
import psycopg2

%pylab inline

pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)
```

    Populating the interactive namespace from numpy and matplotlib



```python
gpd_map = gpd.read_file('/home/lorenzo/Documents/San_Francisco/Bureau of Fire Prevention Districts - Fire Department/')
gpd_map.crs
```




    {'init': 'epsg:4326'}




```python
ax = gpd_map.plot(figsize=(15, 18), color='whitesmoke', edgecolor='dimgray')
ax.axis('off');
plt.title('San Francisco City Fire Stations', fontsize=20);
```


![png](assets/images/20190226/output_3_0.png)


The figure above shows an empty map of San Francisco City fire stations. The succeeding sections added the fire stations are numbered points on the map.


```python
df_stations = pd.read_csv('/home/lorenzo/Documents/San_Francisco/City_Facilities_-_Fire_Department_Jurisdiction_or_Leased.csv')
# df_stations.head(1)
```


```python
df_stations_geom = df_stations[['common_name', 'longitude', 'latitude']]
df_stations_geom.drop_duplicates(inplace=True)
# df_stations_geom
```

    /home/lorenzo/anaconda/envs/gsa/lib/python3.7/site-packages/ipykernel_launcher.py:2: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame
    
    See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
      



```python
geometry = [Point(xy) for xy in zip(df_stations_geom['longitude'], 
                                    df_stations_geom['latitude'])]
crs = {'init': 'epsg:4326'}
gdf_stations_geom = gpd.GeoDataFrame(df_stations_geom, crs=crs, geometry=geometry)
```


```python
ax = gpd_map.plot(figsize=(15, 18), color='whitesmoke', edgecolor='dimgray')
ax.axis('off');
gdf_stations_geom.plot(ax=ax, color='red', alpha=0.3)
plt.title('San Francisco City Fire Stations', fontsize=20)
for x, y, label in zip(gdf_stations_geom.geometry.x, gdf_stations_geom.geometry.y, gdf_stations_geom.index):
    ax.annotate(label, xy=(x, y), xytext=(3, 3), textcoords="offset points");
```


![png](assets/images/20190226/output_8_0.png)

