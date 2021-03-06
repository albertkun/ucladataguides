.. _excel_cleaning:

Cleaning Data in Microsoft Excel
======================================================

Getting Started
---------------

Note: This tutorial uses Los Angeles Police Department Arrest data
filtered for the month of January downloaded from Los Angeles Open Data
portal (see: :ref:`data_portal` )

How to open CSV files
---------------------

1. Go to File -> Open

2. Select “Text” file
..

|ex_image0|

3. Select the “LAPD_arrests_2015_january.csv” file:
..

|ex_image1|

4. Excel always provides a summary of selected information near the bottom:
..

|ex_image2| 

Before going forward, let’s make sure our data columns are in good
order:

   ARST_DATE should be a date field, and ARST_TM should be a Time Field.

5. Select the columns:

..

|ex_image3|

6. Select dropdown box near the top:
..

|ex_image4|

7. Then choose “Short Date”:

..

|ex_image5|

8. For ARST_TM choose “Time”:

..

|ex_image6|

9. Do the same for BKG_DT and BKG_TM as well.

Formulas
--------

Excel is a spreadsheet program, which means it is made up of rows and
columns: one giant table. One of the most powerful tools is formulas,
which means starting a cell with an “=”

Go ahead and find an empty cell so we can start our formula:

..

|ex_image7|

S2 looks like a good spot.

The most basic formula we will use is to combine columns together:
::
   = A1 & B1

Every Excel formula relies on using the cells of a table in order to
work. For example A1 is the very first cell in the spreadsheet. If you
want to combine the contents in the first cell together with the second
column, then you can use “=\ A1\ &\ B1\ ”

Question: Whats the formula to combine the Lat(\ Q2) and Long(\ R2) columns into one?
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''                                                                                     

If you simply add the two, it might look a little messy, so we should add a space in between columns by the following formula:
::
   = A1 &“ “& B1

You will notice that the “ “symbols acts as a seperator. You can go
ahead and put anything in between those symbols and it will appear in
between the result.

Question: Whats the formula to combine the Lat(\ Q2) and Long(\ R2) columns into one with a comma in between?
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''                                                                                                             

Sorting
-------

In the top part of the menu you can select “Sort”:

..

|ex_image8|

A dropdown arrow will now be shown next to the first row (also known as
the header)

..

|ex_image9|

When clicking it, you can choose to sort the information in different
ways:

..

|ex_image10|

We will sort the data from highest to lowest arrest date:

..

|ex_image11|

Feel free to explore sorting the data!

Filtering
---------

You can also filter the data by using the Checkboxes or the Filter By
box below the Sort options:

..

|ex_image12|

Different data types will have different filter options, feel free to
try it out and answer this question:

Question: How many arrests were there on January 1st?
'''''''''''''''''''''''''''''''''''''''''''''''''''''

Splitting content from one cell into two cells
----------------------------------------------

Sometimes a dataset may include coordinates, which can easily be
imported into ArcGIS Online to visualize spatially. However, in order to
import seamlessly the latitude and longitude need to be in two separate
columns. Follow the instructions below if the coordinates are in one
column.

1. Select the cell or cells whose contents you want to split.

   a. Important: When you split the contents, they will overwrite the
      contents in the next cell to the right, so make sure to have an
      empty column there.

..

|ex_image13|

2. On the Data tab, in the Data Tools group, click Text to Columns. The Convert Text to Columns Wizard opens.


   
..
      |ex_image14|

3. Choose Delimited if it is not already selected, and then click Next.
..
   |ex_image15|

4. Select the delimiter or delimiters to define the places where you
   want to split the cell content. The Data preview section shows you
   what your content would look like. Click Next.

..

   |ex_image16|

5. In the Column data format area, select the data format for the new
   columns. By default, the columns have the same data format as the
   original cell. Click Finish.


   
..
      |ex_image17|

6. The coordinates are now split into two columns based on the comma
   delimiter. However, the new columns still have the single
   parenthesis. To remove the parentheses add two new columns to the
   right of each new coordinate column.

..

|ex_image18|

..

|ex_image19|

7. Type the following equation in the cell to the right of the first
   column: =RIGHT(Q2, LEN(Q2)-1).


   
..
      |ex_image20|

8. To copy the equation to the remaining rows, select the cell and hover
   over the bottom right corner until the cursor becomes a cross.
   Double-click.

..

|ex_image21|

9. Type the following equation in the cell to the right of the second
   new location column: =LEFT(S2, LEN(S2)-1). Repeat the process for
   the longitude column and copy the formula into the remaining
   cells. Make sure to label the new columns ‘lat’ and ‘lon’.


   
..
      |ex_image22|

Leading Zeros
-------------

1. Sometimes when moving data between software, leading zeros are
   dropped which change the way you can use a particular dataset.
   This is particularly true when working with zip codes.


   
..
      |ex_image23|

2. To add back the leading zeros, highlight the column and right-click
   to select Format Cells. Then select Custom.


   
..
      |ex_image24|

3. Type ‘00000’ in the Type field and click ‘OK’..
   .\ 
|ex_image25|

4. Leading zeros have now been added back to your field!


   
..
      |ex_image26|

Next Guide: Joining Data in QGIS
--------------------------------

Sometimes you want to summarize data by location. For example you want
to see the number of arrests by zipcodes or neighborhoods. To do this,
you need to do what is called a spatial join.

.. |ex_image0| image:: ../media/ex_image0.png
   :width: 6.5in
   :height: 2.79167in
.. |ex_image1| image:: ../media/ex_image1.png
   :width: 5.13021in
   :height: 3.67434in
.. |ex_image2| image:: ../media/ex_image2.png
   :width: 4.82292in
   :height: 3.98958in
.. |ex_image3| image:: ../media/ex_image3.png
   :width: 6.5in
   :height: 2.88889in
.. |ex_image4| image:: ../media/ex_image4.png
   :width: 6.5in
   :height: 2.88889in
.. |ex_image5| image:: ../media/ex_image5.png
   :width: 5.64478in
   :height: 2.50521in
.. |ex_image6| image:: ../media/ex_image6.png
   :width: 5.60532in
   :height: 2.49479in
.. |ex_image7| image:: ../media/ex_image7.png
   :width: 1.9375in
   :height: 1.30208in
.. |ex_image8| image:: ../media/ex_image8.png
   :width: 6.5in
   :height: 1.76389in
.. |ex_image9| image:: ../media/ex_image9.png
   :width: 6.5in
   :height: 1.56944in
.. |ex_image10| image:: ../media/ex_image10.png
   :width: 1.94814in
   :height: 3.03646in
.. |ex_image11| image:: ../media/ex_image11.png
   :width: 2.75521in
   :height: 3.67874in
.. |ex_image12| image:: ../media/ex_image12.png
   :width: 2.15104in
   :height: 2.97414in
.. |ex_image13| image:: ../media/ex_image13.png
   :width: 5.31771in
   :height: 4.21837in
.. |ex_image14| image:: ../media/ex_image14.png
   :width: 6.5in
   :height: .85in
.. |ex_image15| image:: ../media/ex_image15.png
   :width: 6.5in
   :height: 4.625in
.. |ex_image16| image:: ../media/ex_image16.png
   :width: 6.5in
   :height: 4.625in
.. |ex_image17| image:: ../media/ex_image17.png
   :width: 6.5in
   :height: 4.625in
.. |ex_image18| image:: ../media/ex_image18.png
   :width: 5.08333in
   :height: 4.52107in
.. |ex_image19| image:: ../media/ex_image19.png
   :width: 5.13021in
   :height: 4.57115in
.. |ex_image20| image:: ../media/ex_image20.png
   :width: 6.57813in
   :height: 1.14612in
.. |ex_image21| image:: ../media/ex_image21.png
   :width: 4.76563in
   :height: 2.15102in
.. |ex_image22| image:: ../media/ex_image22.png
   :width: 3.98438in
   :height: 3.74249in
.. |ex_image23| image:: ../media/ex_image23.png
   :width: 3.83854in
   :height: 3.05662in
.. |ex_image24| image:: ../media/ex_image24.png
   :width: 4.99479in
   :height: 4.45049in
.. |ex_image25| image:: ../media/ex_image25.png
   :width: 4.81566in
   :height: 4.29688in
.. |ex_image26| image:: ../media/ex_image26.png
   :width: 4.53125in
   :height: 2.86458in
