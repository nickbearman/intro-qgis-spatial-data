---
  output: pdf_document
---
  <!-- complied with pandoc -V geometry:margin=1in postcodes.md -s -o postcodes.pdf -->
  
# Postcodes

In the session today we showed you how to plot data with XY coordinate data. We used the world-cities data which had coordinates in latitude-longitude and we used the Add XY data tool in QGIS to turn the coordinates into spatial data and to add them to the GIS project. 

What if we have some address data like the list shown below? How do we get that into QGIS?

    14 Well Grove, Whitefield, Manchester M45 7SQ, UK
    80 Wroxham Rd, Norwich NR7 8EX, UK
    14A Wortley Rd, Wotton-under-Edge GL12 7JU, UK

With most things in GIS, we have a couple of options. Today, we will use a website called www.doogal.co.uk which will geocode the addresses we have. Geocoding takes a text based address, and returns a set of coordinates. 

- Go to `https://www.doogal.co.uk/BatchGeocoding.php` 
- Copy and paste the text from `postcode-input-file.csv` into the 'Addresses' box on the webpage 
- Hit **Geocode** 
<!--  
blah for spacing
-->

- Wait a short time while the geocoding takes place 
- When it is complete, click **'Download text'** 
- Save the file (`locations.csv`) somewhere you can find it later 


*Things to remember:
- There must not be any quote marks (`"`) in the addresses 
- Always check the output - not all of the geocoding may be successful *

- Open **QGIS** 
- As before, click **Layer > Add Layer > Add Delimited Text Layer...** 
- Click **Browse** and find the `locations.csv` file 
- Select **First record has field names** 
- Check the output at the bottom of the screen - does it look sensible? 
- Set the coordinates in the X and Y fields - we have both latitude-longitude and eastings-northings. As our data is for Great Britain, we can use eastings and northings (British National Grid). 
<!-- - Your **Create a Layer from a Delimited Text File** window shoud look like this: 

![Create a Layer from a Delimited Text File](add-delimited-layer.png){ width=40% }
-->

- Click **Ok** 
- QGIS will ask you select the Coordinate System the data are using - select **British National Grid** (27700) as before 
- Check the data - do they look sensible for the addresses? *(You may need to add some base map data)* 
  
  
  
*This was written by Dr. Nick Bearman (nick@clearmapping.co.uk). Thanks to Chris Bell for providing the geocoding resource at https://www.doogal.co.uk. This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/deed.en. The latest version of the PDF is available from https://github.com/nickbearman/intro-qgis-spatial-data. This version was created on 19th November 2017. *
