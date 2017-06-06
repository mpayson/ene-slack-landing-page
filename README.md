# Slack Landing Page

This is an adaption of the awesome wind-js visualizations (https://github.com/Esri/wind-js) to create a landing page for the esri new employee community. Read-me information from the original repo is copied below.

## How it works

The code for this project uses nothing but an HTML5 Canvas element and pure Javascript. The data come from the Global Forecast System which produces a large variety of datasets as continuous global gridded datasets (more info below). The data is passed into a JS class called `Windy` which takes the bounds of the map, the data, and the canvas element and then applies a [Bilinear Interpolation](http://en.wikipedia.org/wiki/Bilinear_interpolation) to generate a smooth surface. Once the surface has been generated a function randomly places "particles" onto the canvas at random x/y points. Each particle is then "evolved", moving in a direction and at a velocity dictated by the interpolated surface.

## The Data

Before [GFS data](http://nomads.ncdc.noaa.gov/data.php?name=access#hires_weather_datasets) can be used with this code it has to be converted into JSON. To do this we used another awesome project by [@cambecc](https://github.com/cambecc) called [`grib2json`](https://github.com/cambecc/grib2json). That tool converts data in the GRIB2 file format into a JSON structure with the grid represented as an array. An example result of that tool can be seen in the `gfs.json` file.

## Resources

* https://github.com/cambecc/earth
* http://earth.nullschool.net/
* [http://nomads.ncdc.noaa.gov/data.php...](http://nomads.ncdc.noaa.gov/data.php?name=access#hires_weather_datasets)
* http://developers.arcgis.com
* [twitter@esri](http://twitter.com/esri)

## Issues

Find a bug or want to request a new feature?  Please let us know by submitting an issue.

## Credit

All the credit for this work goes to [@cambecc](https://github.com/cambecc) for creating [cambecc/earth](https://github.com/cambecc/earth). The majority of this code is directly taken from there, since it's utterly awesome.

## Licensing

This project inherits an MIT license from [cambecc/earth](https://github.com/cambecc/earth) because 95% of the code here was copied from that project.

A copy of the license is available in the repository's [license.txt]( https://raw.github.com/Esri/wind-js/master/license.txt) file.
