Data visualization is the graphical representation of information and
data. By using visual elements like charts, graphs, and maps, data
visualization tools provide an accessible way to see and **understand
trends, outliers, and patterns in data**.

Tableau is a data visualization software. It allows anyone to upload
data from any source and instantly create interactive visualizations aka
Dashboards.
`Here <https://public.tableau.com/en-us/gallery/?tab=viz-of-the-day&type=viz-of-the-day>`__
some of the great examples of how others have used Tableau.

The purpose of this tutorial is to give everyone the basic tools
necessary to start using Tableau. If you believe Tableau meets your
needs for visualizing your data, please visit `this
site <https://www.tableau.com/learn/training>`__, where you can find a
more detailed overview of tableau.

Outline:

1. Connect to Data

2. Create Visualizations

   a. Table

   b. Bar

   c. Linear (Trend)

   d. Basic Map

3. Dashboard

Connect to Data

For the purposes of this exercise, we will use the
“ARREST_DATA_2017_2018”. Please download the following dataset to follow
along: \________\_

When you open Tableau, the first screen should look like this:

|image0|

Since we are working with a CSV (comma delimited file), click on “Text
File” to the left. What should result is a screen like this:

|image1|

The connection should be the main dataset you connected to. Your data
should display in the center. If you click “Update Now” you should be
able to get a preview (first 1,000 rows) of the dataset you imported.

|image2|

Over the variable names are various symbols. These are the data types
that Tableau automatically assigned to each of the variable names. If
the values in your dataset looked like a number you should see a “#”
sign. If you brought in something that looks like a date, you’ll see a
calendar icon, and if your data looks like a bunch of character strings,
you’ll see an “Abc” symbol. Not shown here is a logical type variable
(True/False). Those will appear as “T|F”.

You’ll also see that some variables are green or blue. This is something
more unique to Tableau and unique to numerical variable types. If your
variable is green, Tableau read the values of your numerical variable as
“Continuous”. In other words, as a form of metric. If it’s blue, it read
the values of your numerical variable as “Discrete”. In other words, as
a form of a category.

This is different from something inherent that Tableau does which is
assign your data as “Dimensions” and “Measures” which are inherent in
the Tableau language to know the type of view to use for your
visualization.

These will make more sense as we get deeper into it. For now let’s open
up our first “Sheet”. Highlighted in orange at the bottom is “Sheet1”.
Please click on that to continue.

Create Visualizations

When you open up your sheet, you should first see a screen like this:

|image3|

As mentioned before, are our “Dimensions” and “Measures”. This is one
way that Tableau will know what graph to generate. Under “Dimensions”
are our variables that tableau assigned as “discrete” variables. Under
“Measures” will rest what Tableau assigned as “continuous” variables.

Tableau will not always do this correctly. For example, our City Council
District variable, though they are numbers, are actually categories. In
order to change this, right click or left click on the down arrow when
you highlight over the variable. See below:

|image4|

Then click on “Convert to Dimension”. Our City Council Dist variable
should then appear in our Dimensions section. See Below:

|image5|

We also have the option to turn our variable into “Continuous” after
it’s put into our Dimensions shelf, but we wouldn’t want to because even
though it’s a numerical value, it acts more like a distinct discrete
variable. To read more about this distinction please refer
`here <https://help.tableau.com/current/pro/desktop/en-us/datafields_typesandroles.htm>`__.

Next to our Dimensions and Measures is the main body of the sheet:

|image6|

The big white area will be where our visualizations will appear. The
“Filters” is if we want to filter our visualization based on certain
values. For example, if we wanted to visualize only “Females”, we would
place our Gender variable here. “Marks” is where we will we can
customize our visualizations based on how we want our visualization to
look. For example if we want to separate our visualization based on our
different racial categories, we would drag our race variables into one
of the Marks. If we wanted to differentiate it by color we would drag
the variable to the Color box.

We have a columns and rows which is where the variables need to go to
visualize. “Pages” will be unimportant for our purposes, but if you wish
to know please refer
`here <https://www.dummies.com/programming/big-data/big-data-visualization/how-to-use-the-pages-shelf-in-tableau/>`__.

This makes sense as you work more with Tableau. For now, let’s create a
couple of simple visualizations.

Create a Table

Let’s make our first visualization.

Say we wanted to create a table with the number of arrests by Race, we
would first double click our Race variable (“Race Cat”). Our variable
would appear on the columns shelf and we’d see the following empty
table:

|image7|

If we wanted to populate this table with the number of arrests, we’d
have to choose a variable from our “Measures” section. Since each
row/record in our dataset is an arrest, we can double click the “Number
of Records” variable (Tableau generated variable). What you should see
is “Number of Records appear on the “Marks” shelf and a table that is
now populated with numbers:

|image8|

We’ve created our first visualization!

Now say we wanted to cross-tab Gender into this. In other words see how
many arrests look when we cross race and gender together. If we now
click on our Gender variable (“SEX” in our dataset) we should see a
cross tab of Gender and Race:

|image9|

If we didn’t want just a count and would rather want percentage, we can
change that by right clicking our “Number of Records” variable under
“Marks” and clicking on “Quick Table Calculations” then “Percentage of
Total”:

|image10|

That should result in a table that looks like below:

|image11|

We can see now that there’s a greater proportion of males in our LatinX
population as opposed to our other racial groups in our data.

We can name this table if we double click on either the “Sheet 1” in our
main visualization space or in the tab below. Let’s rename this to
“Demographic Exploration”. Our final table should look like below:

|image12|

Tables are one way to visualize data and Tableau has a way to quickly
create these tables for you. We will now go on other more “visual” based
visualizations.

Create a Bar Graph

Create a new sheet by clicking on this icon in the bottom tabs:
|image13|

For this example, let’s say we are interested in how many people are
being arrested for each City Council District. Let’s double click on
“Number of Records” in the Measure section, then click on “City Council
District”. What you should see is our desired bar graph. See below:

|image14|

If what you’re seeing is horizontal lines rather than vertical lines. On
the top menu bar, you should see a symbol that looks like this:
|image15|

That will change your graph from a horizontal to a vertical one.

Does your visualization actually look like a table? This is because the
order in which you clicked on these variables mattered to tableau to
automatically generate visualizations.

If you click on “City Council District” then “Number of Records”, you’ll
probably see something like this:

|image16|

If that’s the case, you can start over and click on “Number of Records”
first, then “City Council Districts”, but there’s no way you can
memorize which order produces what visualization. In which case there’s
a handy shortcut in the top right of the menu bar: |image17|

The “Show Me” menu gives you the option for quickly turning the
visualization shown to another type of visualization.

|image18|

It even gives you a recommend visualization which is usually boxed in
orange. Click on the bar graph visualization on the left, third row
down.

That should give you a horizontal bar graph in which you can use what
was mentioned before to turn it into a vertical bar graph.

Say for we also wanted to show how each of these different districts
arrests looked by Race. As mentioned previously, the way to do that is
for using our “Marks” shelf. Let’s drag “Race Cat” into the “Color” box
in the “Marks” shelf. What you should see is the visualization below:

|image19|

The bar graph is now stacked by our different racial categories. If we
wanted to actually take a look at the numbers for each of these, let’s
drag the “Number of Records” to the “Label” box. You should see the
total number of record for each bar and each racial category. If we
wanted to see percentage, we’d right click and do a quick table
calculation (as we’ve done before) and click on percentage of total.

The percentages will look wrong at first which is because currently it’s
calculating across, rather than down (per column). So on the right click
menu click “Compute Using” then “Table (down)”.

Your final table should look like below:

|image20|

You can play around with the visualization here. Add other variables
into the “Marks” shelf, switch out colors, change your labels, etc. If
it starts getting out of control, you can always just start over.

Let’s rename this visualization to “Bar Graph of Arrests”

Create a Linear Trend

Our next example will be to create a linear trend. Say for example,
you’d like to see how arrests look like over a period of time. We’d want
something like a line/trend graph to be able to illustrate this.

To get the first set of graphs set up, we’d first double click on
“Number of Records” then our date variable which is “Arrest Date”. What
you should see is something like the graph below.

|image21|

This is a version of our line graph, but it’s currently only showing
year totals for 2017 and 2018. There’s a plus sign, next to the
“YEAR(Arrest Date)” in the columns section. Click on that once and you
should get a graph that looks like below:

|image22|

Now our graph is separated by Quarters. If you click on the plus sign
again next to “QUARTER(Arrest Date)” then it splits itself into months.

|image23|

Though this would technically be what we would want, the graph currently
looks disjointed and it awkwardly separates by Quarters and Years. We’d
rather like to see one continuous graph.

The reason why it does this is because our “Arrest Date” variable is
currently a “Discrete” variable. Thus our values are separated by the
Month/Quarter/Year categories. Since we don’t want those distinct
categories in our trend graph, we’ll have to convert it to continuous.

Click the minus button next to “YEAR(Arrest Date)” to condense
everything to year. Then right click the variable. What you should see
is the following menu:

|image24|

Click on the second set of “Month”, the one that says “May 2015” next to
it. The resulting graph is what we want to see:

|image25|

It also automatically converted our “Discrete” date variable into a
continuous one (It’s now green instead of blue). Take your time to play
around with the Marks at this time to see how different variables look
when you place them in there.

Let’s save this sheet as “Trend Over Time”.

Create a Basic Map

The last thing we want to do is create a basic map through Tableau. On
the left are our “Longitude” and “Latitude” variables with a little
globe to the left to indicate that it’s a “Geography” type variable.
Note: We are NOT using the ones that are “generated”. Those are ones
that Tableau created which don’t matter to us because we have our
Longitude and Latitude variables.

Let’s double click on “Latitude” and “Longitude”. What you see should be
something like below:

|image26|

A basic map is created, but there’s only one dot. The reason why it’s
doing this is because it is a “Measure” it will automatically do some
sort of calculation here. In this instance we see “AVG” (Average)
encasing our Longitude and Latitude variables. In this case it’s mapping
the average longitude and average latitude, which is one value.

We don’t want anything calculated so let’s right click our
“AVG(Longitude)” variable in the Column shelf and we should see the list
of options like shown below:

|image27|

Let’s click on “Dimension”. We should see that Longitude is no longer
encased by “AVG”. Let’s also do the same thing for “AVG(Latitude)”. The
resulting visualization should look like the below:

|image28|

Since the dots look a little too clustered together now, I’m going to
reduce the size of the dots by going to the “Marks” shelf and click on
“Size” like below:

|image29|

Let’s slide the slider to the left. You can go however much you want,
but the resulting dots should be smaller now. Here is how mine looks:

|image30|

For the purposes of this exercise, say we only want to see the dots of
all the Females who are arrested. We will now work with our “Filter”
shelf. Let’s drag our “SEX” variable into our “Filter” shelf. When you
do, a pop-up will appear that looks like below:

|image31|

This will ask us directly what we want to filter by. For now let’s
select “All” then press “OK”. We now have our “SEX” variable resting on
our shelf:

|image32|

Let’s right click on “SEX” and click on “Show Filter”. What results is
our map with a filter that now appears on the right:

|image33|

If you click through the different filters. The map will change based on
what you decide to filter by. If we wanted to see how Arrests look for
“Females”, we’d unclick our “Male” values. The resulting maps should
look like below:

|image34|

One of the things I like to do is change how the filter looks like. This
is entirely up to you though. If you want to change how the filter
looks, hover your mouse to the filter and three icons will appear. Click
on the little down arrow. From there we’ll see, as options, a host of
ways we can display the filter:

|image35|

I personally like “Single Value (list)”. I will be clicking on that. Now
my filter will be single click and I’ll be able to switch easily from
“M” and “F”.

|image36|

Let’s do the same thing for Race. Drag “Race Cat” into our “Filters”
shelf. Go through the same process detailed for “SEX” above. The
resulting map should look like below:

|image37|

This map now displays all arrests from 2017-2018 for Black Females.

Let’s name this “Map of Arrests”

We’ve created our last visualization for this exercise. What we will go
over next is how to put this all together into a “Dashboard” which is
one way you can have people interacting and playing with the underlying
data so that they may derive insight.

Create a Dashboard

To Create a new Dashboard click on this icon: |image38|

What you should see is a screen like below:

|image39|

On the left is our size. This may look different for you. You can adjust
the size of your dashboard to however width and length you’d like. For
now let’s change our size to “Automatic”. To do so click on the little
arrow under our “Size” shelf. Click on the little arrow again on the
right of “Range” then click on “Automatic”.

|image40|

Under the size are our created “Sheets”. Click on “Map of Arrests”, then
“Bar Graph of Arrests”, then “Trend Over Time”, then “Demographic
Exploration”. What should result is the Dashboard below:

|image41|

This is what Tableau is most popular for. The ability to see multiple
visualization on one “Dashboard”. You’ll see filters on the right as
well as our four sheets.

Let’s edit our Dashboard a little bit.

Our table looks kind of small. Let’s fix how this sheet fits in this
dashboard. Click on our “Demographic Exploration” sheet. The sheet will
be highlighted in grey. Four icons will appear on the right. Click on
the down arrow and you’ll see a list of options:

|image42|

Click on “Fit” then “Fit Width” which will give us the most visually
pleasing display of this table. You can play around with this to see
which one you believe looks best.

Now on the right are our filters which we created when we did our Map
visualization. When you import sheets into a dashboard, the dashboard
will also import the filters. However, for now, the filters will only
filter our map (try it out). We can however make this filter also drive
all of the other sheets in the dashboard.

Let’s click on the “SEX” filter. We’ll see the same grey border appear
and a down arrow that comes along with it. In that menu, you’ll see
these options:

|image43|

Click on “Apply to Worksheets” then “All Using This Data Source”. Now
everything will be driven by this filter. Make sure to try it out
yourself and see how everything changes!

You can interact and click on various parts of each sheet and it will
highlight, but say you also want the visualization to change based on
what you click in the Dashboard itself. You can create an “Action” to do
so.

For example, in our bar graph are the different council district
numbers. Click on “14” on the x-axis. What you should see is the bar
highlighted like below:

|image44|

That’s cool in and of itself, but say we want to also change everything
else so that all the other visualizations we’re seeing are only those in
City Council District 14.

On the very top of our menu you’ll see a menu for “Dashboard” (may look
different if using Windows):

|image45|

Click on that menu and go to “Actions…”

|image46|

A pop-up menu should pop up. From there click “Add Action >” then
“Filter”

|image47|

Another pop up should appear like below:

|image48|

You’ll have the sheet you want the action to start from and the
resulting sheets you want to change. We want to be able to click on the
“14” on the bar char x-axis and change all the other sheets in the
dashboard. You’ll want to de-select all other sheets in the “Source
Sheets” and select all, but the Bar Graph sheet for our “Target Sheets”.

On the right, we have the option to “Run Action On” and a choice of
Hover, Select, and Menu. We want to have it so that it changes when we
click on it, so we’ll have to change to “Select”.

Lastly, there’s a “Clearing the selection will:” option on the right.
This is what you want to happen to the other sheets once you de-select
“14” on the bar chart. For now we’ll have it “Show all values” again,
but this is something you can play with in accordance to how you want to
present the visualization.

Let’s rename this action above in “Name:” to “Bar Chart Action”.

When you finish putting the action together, your Action criteria should
look like below:

|image49|

When your Action criteria matches above, click “OK” then “OK” again in
the previous dialog box.

Now when you click on the “14” on the x-axis of the bar chart all the
other sheets should change. The dashboard should look like below:

|image50|

Our Trend over time changed as well as our map.

People place multiple actions onto dashboards and as a result have a
full working data playground.

This is a simple dashboard we put together, but Tableau is a powerful
tool that allows people to create interactive multi-faceted
visualizations with their data.

If you believe that Tableau is a tool you’d like to become more
acquainted with, as mentioned before, please visit `this
site <https://www.tableau.com/learn/training>`__ which hosts a lot of
detailed videos on all the moving parts of this program.

.. |image0| image:: media/image1.png
   :width: 6.34021in
   :height: 4.05814in
.. |image1| image:: media/image2.png
   :width: 6.41303in
   :height: 4.11622in
.. |image2| image:: media/image3.tiff
   :width: 7.5in
   :height: 0.88264in
.. |image3| image:: media/image4.png
   :width: 6.0911in
   :height: 3.9186in
.. |image4| image:: media/image5.png
   :width: 2.91301in
   :height: 3.12791in
.. |image5| image:: media/image6.png
   :width: 1.75414in
   :height: 3.51647in
.. |image6| image:: media/image7.png
   :width: 6.95041in
   :height: 4.60465in
.. |image7| image:: media/image8.png
   :width: 3.37209in
   :height: 2.58858in
.. |image8| image:: media/image9.png
   :width: 1.80233in
   :height: 1.33721in
.. |image9| image:: media/image10.png
   :width: 2.06977in
   :height: 1.32426in
.. |image10| image:: media/image11.png
   :width: 4.13798in
   :height: 4.7303in
.. |image11| image:: media/image12.png
   :width: 2.47674in
   :height: 1.52676in
.. |image12| image:: media/image13.png
   :width: 3.22713in
   :height: 2.10465in
.. |image13| image:: media/image14.png
   :width: 0.44444in
   :height: 0.43056in
.. |image14| image:: media/image15.png
   :width: 5.83721in
   :height: 4.10821in
.. |image15| image:: media/image16.png
   :width: 0.55556in
   :height: 0.45833in
.. |image16| image:: media/image17.png
   :width: 1.45342in
   :height: 3.27713in
.. |image17| image:: media/image18.png
   :width: 1.25in
   :height: 0.45833in
.. |image18| image:: media/image19.png
   :width: 1.33988in
   :height: 3.21519in
.. |image19| image:: media/image20.png
   :width: 7.5in
   :height: 4.575in
.. |image20| image:: media/image21.png
   :width: 7.5in
   :height: 4.57222in
.. |image21| image:: media/image22.png
   :width: 1.98594in
   :height: 2.46028in
.. |image22| image:: media/image23.png
   :width: 4.30529in
   :height: 3.23256in
.. |image23| image:: media/image24.png
   :width: 5.80233in
   :height: 4.20937in
.. |image24| image:: media/image25.png
   :width: 2.95895in
   :height: 5.97674in
.. |image25| image:: media/image26.png
   :width: 4.9807in
   :height: 3.59302in
.. |image26| image:: media/image27.png
   :width: 6.37209in
   :height: 4.94722in
.. |image27| image:: media/image28.png
   :width: 2.1239in
   :height: 2.83721in
.. |image28| image:: media/image29.png
   :width: 7.5in
   :height: 5.54167in
.. |image29| image:: media/image30.png
   :width: 2.27907in
   :height: 1.23135in
.. |image30| image:: media/image31.png
   :width: 7.5in
   :height: 5.52569in
.. |image31| image:: media/image32.png
   :width: 4.89389in
   :height: 4.78196in
.. |image32| image:: media/image33.png
   :width: 1.97744in
   :height: 4.38372in
.. |image33| image:: media/image34.png
   :width: 6.52326in
   :height: 4.26971in
.. |image34| image:: media/image35.png
   :width: 5.73964in
   :height: 3.74352in
.. |image35| image:: media/image36.png
   :width: 2.74049in
   :height: 4.15116in
.. |image36| image:: media/image37.png
   :width: 1.88372in
   :height: 1.18307in
.. |image37| image:: media/image38.png
   :width: 7.5in
   :height: 4.90625in
.. |image38| image:: media/image39.png
   :width: 0.61111in
   :height: 0.63889in
.. |image39| image:: media/image40.png
   :width: 7.50271in
   :height: 4.60861in
.. |image40| image:: media/image41.png
   :width: 2.15642in
   :height: 2.41634in
.. |image41| image:: media/image42.png
   :width: 7.5in
   :height: 4.89653in
.. |image42| image:: media/image43.png
   :width: 7.5in
   :height: 4.46944in
.. |image43| image:: media/image44.png
   :width: 5.54726in
   :height: 6.59302in
.. |image44| image:: media/image45.png
   :width: 5.68605in
   :height: 4.18293in
.. |image45| image:: media/image46.png
   :width: 7.5in
   :height: 0.34167in
.. |image46| image:: media/image47.png
   :width: 3.36115in
   :height: 3.17442in
.. |image47| image:: media/image48.png
   :width: 7.5in
   :height: 4.36806in
.. |image48| image:: media/image49.png
   :width: 6.38866in
   :height: 7.15116in
.. |image49| image:: media/image50.png
   :width: 6.00676in
   :height: 6.60465in
.. |image50| image:: media/image51.png
   :width: 7.5in
   :height: 4.90486in
