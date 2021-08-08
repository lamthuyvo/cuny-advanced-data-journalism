## Intro
GeoPandas is an extremely useful and mostly user-friendly tool for doing basic GIS analysis and plotting in Python. I use it more frequently than QGIS or other tools because it integrates nicely with Jupyter Notebooks and uses Pandas under the hood, both of which are regular parts of my daily data journalism toolkit.

It's important to realize that GeoPandas is really just a nice wrapper around a bunch of other useful Python libraries including Pandas, Matplotlib, Fiona, Shapely and others. If you want to do something complicated that's not covered by the GeoPandas documentation, there's a good chance you can still do it by looking at the documentation for one of those other libraries.

## Getting started

"Cloning" a Github repo is pretty easy. You can download a zip, but it's actually a little easier to use the command line since you have to use the command line to start the project anyway. 

1. Click the green "clone or download" button at the top right of the file list on this page.
2. Copy that URL by clicking the copy button next to it.
3. Open up your terminal and `cd` into a place where you like to keep your projects. Just `cd` into the Desktop if you don't have a place like that.
4. Clone the repo by typing `git clone` and pasting the URL you just copied. The final command should look like:
```
git clone https://github.com/scottpham/cuny_geopandas.git
```
This will download a new folder to your location. You are not "inside" this folder yet. `cd` into it! 

```
cd cuny_geopandas
```

Next, unzip the big data files I've loaded here. Simply open the `data` folder and double click on each of the zipfiles. It should just take a second. 

Finally, install your dependencies. 

In other projects, I would use [Pipenvs](https://github.com/pypa/pipenv) to save my dependencies. For the sake of this class, I want you to create a native virtual environment the way you've been doing all class. You want to install the following libraries: `pandas`, `jupyter`, `geopandas` and `descartes`. This last ones is required for making map graphics.


```
pip install pandas jupyter geopandas descartes
```

That will take 2 - 3 minutes. You can just let it run.

## Data Sources

The unemployment data in `data` comes from the [Bureau of Labor Statistics](
https://www.bls.gov/lau/#cntyaa) "Labor Force data by county, 2018 annual averages". I've cleaned up the column names to make it easier to merge, but otherwise haven't changed anything.

The geographic data comes from the [Census Tigerline](https://www2.census.gov/geo/tiger/TIGER2018/) site, where the most definitive U.S. geographic data comes from. I simplified these files a lot, including removing Hawaii and Alaska for simplicity.

## Helpful links

[GeoPandas reference](http://geopandas.org/install.html)

[Jonathan Soma's excellent GeoPandas tutorials](http://jonathansoma.com/lede/foundations-2017/classes/geopandas/mapping-with-geopandas/)

[Spatial Reference for getting EPSG numbers](http://spatialreference.org/ref/epsg/3310/)

[Pyplot options](https://matplotlib.org/3.0.2/api/_as_gen/matplotlib.pyplot.plot.html#matplotlib.pyplot.plot)

[Spatial join example](https://github.com/datadesk/geopandas-spatial-join-example)

[Matplotlib colormaps](https://matplotlib.org/users/colormaps.html)

[Matplotlib named colors](https://i.stack.imgur.com/lFZum.png)

[Census shapefiles](https://www2.census.gov/geo/tiger/TIGER2018/)

