Quick Visual Guide to Joining Data in QGIS
==========================================

Getting Started
~~~~~~~~~~~~~~~

Note: This tutorial uses data downloaded from Los Angeles Open Data
portal (see: `Quick Visual Guide to Visualizing Data on LA Open Data
Portal <https://drive.google.com/file/d/140rq7sU548VdtYMkiQ8SLIMDLl7smoJE/view?usp=sharing>`__\ )

Download QGIS if you do not have it installed:
\ http://www.qgis.org/en/site/forusers/download.html
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Next download the following datasets:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

http://boundaries.latimes.com/1.0/boundary-set/la-county-neighborhoods-v5/?format=shp\ 
\ http://sandbox.idre.ucla.edu/mapshare/data/usa/census/Los_Angeles_ZipCodes.zip

Most GIS files (also called shapefiles) will be in a zipped format, so
be sure to unzip them!

Mac Example:\ https://asmand.files.wordpress.com/2015/09/unzip-mac.gif

PC Example:\ https://www.youtube.com/watch?v=ZQOYqzGHiDY

How to add vector data
----------------------

1. Click the weird V to the left of the main menu
      \ |qg_image0|

2. Click Browse
      \ |qg_image1|

3. Find the “l.a county neighborhood (v5).shp” file and click “Open”
      \ |qg_image2|

4. Now select open
      \ |qg_image3|

5. Now the vector file should show up in the window:
      \ |qg_image4|

Working with layers:
--------------------

1. Let’s add another GIS file called Los_Angeles_ZipCodes
      \ |qg_image5|

2. Notice what happens right after you add it:
      \ |qg_image6|

3. It appears on top of the La county neighborhood (v5) layer which masks it from view.

4. If you hit the box with the X you can toggle it on and off.
      \ |qg_image7|

5. You can also drag the layer up and down.
      \ |qg_image8|

6. You can right click or cmd + click on the layer to do various things, such
   as open an attribute table, remove the layer, or copy it.
      \ |qg_image9|

7. Let’s click on “Open Attribute Table”:

|qg_image10|

8.  Here you can see all the data that is stored in the file:
       \ |qg_image11|

9.  You can also filter the data to show only certain things by using
       the expression calculator:
       \ |qg_image12|

10. For example, you can see neighborhoods with less than 10 square
       miles large, by using “sqmi < 10”
       \ |qg_image13|

11. Both in the table and map, the yellow rows are what is less than 10 square miles:

|qg_image14|\ 
\ |qg_image15|

12. You can clear the selection by clicking clear:
       \ |qg_image16|

13. If you want, you can go ahead and remove the layer if you’d like.

.. _section-1:

.. _section-2:

.. _section-3:

.. _section-4:

.. _section-5:

Taking data out of QGIS
-----------------------

Sometimes you want to take data out of QGIS to manipulate it in other
software, such as Excel. You can do so, by opening the layer properties
and clicking save as:

|qg_image17|

You can now choose a file type and name, make sure to select “CSV”:

|qg_image18|

Add a CSV file in QGIS 
-----------------------

Start by clicking the comma:
\ |qg_image19|

After finding the file, a new dialogue box will show up. Be sure to have
Lat and Long selected for the X and Y values [X is always Longitude and
Y is always Latitude]:

|qg_image20|

Spatial Joining Data
--------------------

1.  Make sure you have the two layers you want to join together, in this case the LAPD_arrests_2015_january.csv and the Los_Angeles_ZipCodes.

2.  Go to Vector in the menu
       \ |qg_image21|

3.  Then Data Management
       \ |qg_image22|

4.  Then Join Attributes by Location
       \ |qg_image23|

5.  The target layer should be the layer you want the data to go towards, the join layer is the layer you are taking the
information from. So in this case, the Target is the Los Angeles ZipCodes, while the Join is the LAPD_arrests_2015_january.

6.  Make sure to choose “Intersects” for the Geometric Predicate.

7.  Be sure to select “Take a summary of Intersecting Features” and you only need “sum” and “mean” for the Statistics field.

8.  Your text box should look like the following:
       \ |qg_image24|

9.  Click “Run” to run the join.

10. A new layer called “Joined Layer” should show up:
       \ |qg_image25|

11. Go ahead and open the attribute table and see if the “sum” worked!

12. Try and visualize the data like so:

|qg_image26|

Exporting a map
---------------

QGIS has a tool called “Print Composer” to take care of all your map
printing needs. You can find it by going to “File” then “New Print
Composer”

|qg_image27|

After opening a new print composer, you should add a map, which can by
done by going to “Layout” then “Add new map”:

|qg_image28|

Draw a box to add your map:
\ |qg_image29|

|qg_image30|

You can also add text, shapes and other content.

When you are done using QGIS, you can save your project as a QGIS file:

|qg_image31|

.. |qg_image0| image:: ../media/qg_image0.png
   :width: 6.5in
   :height: 3.04167in
.. |qg_image1| image:: ../media/qg_image1.png
   :width: 3.76563in
   :height: 2.04213in
.. |qg_image2| image:: ../media/qg_image2.png
   :width: 6.5in
   :height: 4.13889in
.. |qg_image3| image:: ../media/qg_image3.png
   :width: 4.63021in
   :height: 2.58451in
.. |qg_image4| image:: ../media/qg_image4.png
   :width: 4.83854in
   :height: 3.43505in
.. |qg_image5| image:: ../media/qg_image5.png
   :width: 6.5in
   :height: 4.08333in
.. |qg_image6| image:: ../media/qg_image6.png
   :width: 6.5in
   :height: 3.91667in
.. |qg_image7| image:: ../media/qg_image7.png
   :width: 6.5in
   :height: 3.91667in
.. |qg_image8| image:: ../media/qg_image8.png
   :width: 5.35938in
   :height: 3.21563in
.. |qg_image9| image:: ../media/qg_image9.png
   :width: 6.5in
   :height: 3.91667in
.. |qg_image10| image:: ../media/qg_image10.png
   :width: 5.08854in
   :height: 3.65331in
.. |qg_image11| image:: ../media/qg_image11.png
   :width: 6.5in
   :height: 3.88889in
.. |qg_image12| image:: ../media/qg_image12.png
   :width: 6.5in
   :height: 3.88889in
.. |qg_image13| image:: ../media/qg_image13.png
   :width: 3.47203in
   :height: 2.82813in
.. |qg_image14| image:: ../media/qg_image14.png
   :width: 6.5in
   :height: 3.84722in
.. |qg_image15| image:: ../media/qg_image15.png
   :width: 6.5in
   :height: 3.69444in
.. |qg_image16| image:: ../media/qg_image31.png
   :width: 6.5in
   :height: 3.72222in
.. |qg_image17| image:: ../media/qg_image16.png
   :width: 6.5in
   :height: 4.66667in
.. |qg_image18| image:: ../media/qg_image17.png
   :width: 4.38281in
   :height: 5.21354in
.. |qg_image19| image:: ../media/qg_image18.png
   :width: 3.89063in
   :height: 3.99845in
.. |qg_image20| image:: ../media/qg_image19.png
   :width: 5.14497in
   :height: 3.34896in
.. |qg_image21| image:: ../media/qg_image20.png
   :width: 5.07813in
   :height: 4.06087in
.. |qg_image22| image:: ../media/qg_image21.png
   :width: 3.43229in
   :height: 3.1625in
.. |qg_image23| image:: ../media/qg_image22.png
   :width: 3.49479in
   :height: 3.22364in
.. |qg_image24| image:: ../media/qg_image23.png
   :width: 6.5in
   :height: 4.47222in
.. |qg_image25| image:: ../media/qg_image24.png
   :width: 6.5in
   :height: 3.68056in
.. |qg_image26| image:: ../media/qg_image25.png
   :width: 6.5in
   :height: 3.79167in
.. |qg_image27| image:: ../media/qg_image26.png
   :width: 4.21666in
   :height: 5.28646in
.. |qg_image28| image:: ../media/qg_image27.png
   :width: 6.5in
   :height: 3.95833in
.. |qg_image29| image:: ../media/qg_image28.png
   :width: 6.5in
   :height: 3.98611in
.. |qg_image30| image:: ../media/qg_image29.png
   :width: 6.5in
   :height: 3.98611in
.. |qg_image31| image:: ../media/qg_image30.png
   :width: 5.375in
   :height: 4.01042in
