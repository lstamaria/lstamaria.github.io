
[PostGIS](https://postgis.net/) is a geospatial database extender for PostgreSQL. It allows location queries to be run using SQL. PostGIS can be a little bit tricky to set up via localhost. We would like to come up with steps that we can follow to launch PostGIS. 

To do this, we follow the guidelines step-by-step lifted from Geospatial Analysis class under Prof. Ed David. The following steps are:

1. Create a directory where PostgreSQL would store its data files

```
export POSTGIS_DIR='/any/directory/you/like'

mkdir -p $POSTGIS_DIR

initdb -D $POSTGIS_DIR

pg_ctl -D $POSTGIS_DIR -l $POSTGIS_DIR/logfile start

createdb
```

2. Start the db and create a password for your user (since a lot of psql clients requires a password)

```
psql

> ALTER USER username WITH PASSWORD 'any-password';
```

3. Initialize the postgis plugin

```
> CREATE EXTENSION postgis;

> \q
```

4. Convert PBF to PostGIS data

```
ogr2ogr -f "PostgreSQL" PG:"dbname=username user=username port=5432 host=127.0.0.1" "/location/of/philippines-latest.osm.pbf"
```

5. Convert Shapefiles to PostGIS data

```
psql

> CREATE SCHEMA gadm;

> \q

shp2pgsql -I -s 4326 /location/of/gadm36_PHL_2.shp gadm.ph | psql -h 127.0.0.1 -d edavid -U edavid --port 5432
```

6. To just start the PostGIS server:

```
export POSTGIS_DIR='/directory/of/database/you/set/up'

pg_ctl -D $POSTGIS_DIR -l $POSTGIS_DIR/logfile start
```


```python

```
