# Using QGIS 3 for geocoding
Some quick tests geocoding Finnish addresses in QGIS 3.

## Using the MMQGIS plugin
Load and activate the MMQGIS first. Then open it from the MMQGIS menu in QGIS:


<table style="width:50%">
<tr>
    <td> <img src="images/mmqgis_geocode.png"/> </td>
</tr>
</table>


The plugin requires a CSV file with the addresses in a specific format. For details, see the plugin documentation in the[plugin page](http://michaelminn.com/linux/mmqgis/) (or guess the format from the dialog window). An example CSV file:

<table style="width:50%">
<tr>
    <td> <img src="images/addresses.png"/> </td>
</tr>
</table>

Select the addresses file and run the geocoding:

<table style="width:50%">
<tr>
    <td> <img src="images/mmqgis_dialog.png"/> </td>
</tr>
</table>

A new shapefile is created with the geocoded address (note that unrecognize addresses are saved to the text file you
specified in the dialog box). This is the result when using the OpenStreetmap/Nominatim geocoding service. Note that
you can use Google too but you will need to get an API key (see mmqgis plugin's pages for more info). Our result shapefile looks like this:

<table style="width:30%">
<tr>
  <td> <img src="images/geocoding_result.png"/> </td>
</tr>
</table>

Note that one of the addresses contained only the name of a well known place and the country:
````
  Paikkatietokeskus,,Finland
````
... yet the geocoding worked normally:


<table style="width:50%">
<tr>
  <td> <img src="images/geocoding_result_zoomed.png"/> </td>
</tr>
</table>
