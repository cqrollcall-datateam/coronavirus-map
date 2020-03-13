# coronavirus-map
Python-driven global time lapse of virus spread

This is a mapping time lapse, driven by Python in a Jupyter notebook and from daily updates from Johns Hopkins University, located <a href="https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Confirmed.csv">here</a>.
Note: JHU changed their reporting scheme March 10 for the US. Prior to March 10, Reporting was by County or locale. On March 10, they also started including state totals in addition to continued reporting at the county/local level, resulting in <a href="https://github.com/CSSEGISandData/COVID-19/issues/571">double counts</a> if both state and local levels are included. The time_series_19-covid-Confirmed2.csv file has values at the state level before March 10 that I back-calculated as sums from the county/local level. Daily updates from March 10 on should be made to the state level only.
Curerently the data update process is manual and I'll look to developing that in the code as well.

Code base pulls from:
<a href="https://www.earthdatascience.org/courses/use-data-open-source-python/intro-vector-data-python/spatial-data-vector-shapefiles/intro-to-coordinate-reference-systems-python/">EarthDataScience.org</a>,
<a href="https://github.com/bendoesdata/make-a-map-geopandas/blob/master/Let's%20make%20a%20map!%20Geopandas%20and%20Matplotlib.ipynb">
bendoesdata</a>, and other sources.

Note: this is an <a href="https://github.com/gboeing/osmnx/issues/45#issuecomment-430781178">important update</a> for installing rtree.

Dependancies:</p>
import os</p> 
import numpy as np</p>
import pandas as pd</p>
import matplotlib.pyplot as plt</p>
from matplotlib.ticker import ScalarFormatter</p>
from matplotlib import animation</p>
import seaborn as sns</p>
import geopandas as gpd</p>
from shapely.geometry import Point</p>
import earthpy as et </p>
from datetime import datetime</p>
import matplotlib.image as mpimg</p>
from matplotlib.offsetbox import TextArea, DrawingArea, OffsetImage, AnnotationBbox</p>
from math import log</p>


