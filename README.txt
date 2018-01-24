SAVETREE
V2 Code created: 11/17/17


SAVETREE is a tool developed in Google Earth Engine for the Lassen Volcanic National park, it creates map layers of trends in tree mortality and adds them to the map. The user can select which spectral indices, areas of interest, years, duration and fire history to add. The user can export their new map in the form of TIFF files, and the user can produce graphs which track the changes in the time series for a particular pixel by clicking on the layer.  
Getting Started
These instructions will help you get started using the SAVETREE tool.
Prerequisites
First of all, you will need a Google account that has access to Google Earth Engine. We have set up an account for LVNP at lavo.savetree@gmail.com. You can access this code by going to this link: 
 
Or by signing into lavo.savetree@gmail.com and following this link: https://code.earthengine.google.com/# and finding the Savetree code under “Owner”.
The path is users/savetree/savetree/SAVETREE.




Required packages
The required data for running the script has been loaded into the assets of the lavo.savetree@gmail.com Google Earth Engine account. Generally, the data can be found in the “users/savetree” library in Google Earth Engine. These shapefiles can also be found in the final deliverables package. 


Running SAVETREE
Hit the “run” button in the center panel to make the widget appear. 


Using SAVETREE
The user can do the following things:


* Spectral Index: Choose from NDMI, NDVI, NDWI or NBR to select which spectral index you would like to create a linear regression layer for. The default is NDMI.
* Area of interest: Choose from Lassen Volcanic National Park, Lassen National Forest, DEVELOP T2 Study Area, the Badger Planning area or choose Your asset (below) to perform the analysis on an asset you load yourself see Loading an Asset for instructions on loading your own asset. The default is LVNP.
* End year and duration: The year must be in YYYY format, it is the last year of the duration of the analysis. The duration should be a number less than 20, with the most meaningful results coming from 3-7 years, it is the number of years it will create the time series for. For example, if you put in 1990 and a duration of 3, the analysis will be run on 1988, 1989, and 1990. The defaults are 2016 and 5. 
* Add Coefficient map: Performs the coefficient trend map analysis on the spectral index and area of interest for the duration you supplied ending with the year you specified and adds that layer to the map.
* Add Bivariate map: Performs the Bivariate map analysis on the spectral index and area of interest for the duration you supplied ending with the year you specified and adds that layer to the map.
* Reset Map: Clears all layers. Note: it does not reset the area of interest or any items in the widget. To reset the area of interest, choose a different area of interest from the dropdown before running a new analysis. 
* Fire history start and end years: These years must be in YYYY format. These numbers create a filter for the fire history data where the only data to be added to the map will be fires or treatments that occurred during those years. 
* Fire History Dataset: Select from FRAP Statewide Wildfire Dataset, RX fire, Other treatment, or load your own fire data asset. To load your own asset see Loading an Asset. The wildfire, rx fire and other treatments are FRAP datasets, for more details on the FRAP data and for the most up-to-date data sets please go to http://frap.fire.ca.gov/projects/fire_data/fire_perimeters_index
* Export Coefficient Map: Exports the Coefficient trend layer as a TIFF file. See Exporting a Layer to get details on how to export layers to your Google Drive.
* Export Bivariate Map: Exports the Bivariate map layer as a TIFF file. See Exporting a Layer to get details on how to export layers to your Google Drive.
* Change Inspector: Click on any part of the Coefficient Trend or Bivariate Map layers and a graph of the change during each year for your duration for that particular point will appear at the bottom of the widget. Click the little box with the arrow in the upper right hand corner of the graph to open the graph in a new tab. You can download this graph from this new tab. 


Exporting a Layer
Click on the “Export Coefficient Map” or “Export Bivariate Map” buttons. This will first add the Coefficient or Bivariate analysis layers to the map, and then the tasks tab in the left hand box should turn yellow. Click on the tasks tab, and at the top there should be a file titled with your analysis, area of interest and duration range, there will be a “Run” button next to it. Click on the run button to initiate the image export. You can change the name of the file, and where it is being exported. Once you’ve made your changes, click the blue run button. It will take a few minutes for your asset to be exported to the location you specified. 


Loading an Asset
SAVETREE 2.0 allows the user to input their own assets to run analyses on. To load an asset, click on the "Assets" tab in the upper left hand box of Google Earth Engine, then click the red "new" button. Select "table upload", then double click the red "select" button and find your shapefile on your local computer. Make sure to select all of the shapefile files (you can do this by holding  the ctrl button while you select them), then hit ok. If you look in the upper right hand box, the tasks tab should be highlighted. Your asset is now being uploaded, do not close your browser until it is complete. After a few minutes (between 5-20 depending on the asset) your asset should show up in the left hand box. You should click the share button and make it "Anyone can read". You can now input this asset in the text boxes provided in the widget. The asset structure is users/*YOUR USER NAME HERE*/*YOUR ASSET NAME HERE* for example, the Lassen Volcanic National Park shapefile asset is: users/savetree/LVNP where savetree is the user name for the account, and LVNP is the name of the asset. This shapefile has been hard-coded into the dropdown menus in the widget, but you could copy and paste "users/savetree/LVNP" into the text box and it would still work. For the fire history asset, make sure your fire history data has "YEAR_" as a data field. Years need to be in YYYY format. The filter works by looking for a range of numbers. 


Contact
If you have questions please contact Heather Myers at hmyerscmt@gmail.com or develop.geoinformatics@gmail.com