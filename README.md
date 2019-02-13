## Leaflet Maps with Google Sheets template 

*by [OpenSavannah](https://opensavannah.org), last updated April 10, 2017*

Question: If you have moved beyond simple drag-and-drop point map tools, such as the [BatchGeo](batchgeo) and [Google My Maps](mymaps) tutorials in this book, and want to create point and/or polygon and/or polyline maps, where should you go?

Answer: Copy and customize our open-source template for Leaflet Maps with Google Sheets. Control the map options display data that you upload to your Google Sheet and GitHub repository. No coding skills required, other than pasting one line of code to link your map with your sheet. Requires two free accounts: Google and GitHub.

#### Video and list of features {-}
<iframe width="560" height="315" src="https://www.youtube.com/embed/kUEfB8wD3Vk?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

- Best to show points, polygons, and/or polylines, with table of points in map view
- Free and open-source code template, built on Leaflet and linked to Google Sheets
- Fork the code and host your live map on the web for free with GitHub Pages
- Geocode location data with US Census or Google, using script inside the Google Sheet
- Easy-to-modify data labels and map options in Google Sheet tabs or uploaded CSV files
- Upload your polygon and polyline GeoJSON files, and custom markers, to your GitHub repo
- Show multiple polygon layers, each with their own color legend and ranges (numerical or text)
- Responsive design resizes your maps to display inside most mobile devices

#### Try it {-}
Explore the map or right-click to [view full-screen map in a new tab](https://datavizforall.github.io/leaflet-maps-with-google-sheets/)
<iframe src="https://datavizforall.github.io/leaflet-maps-with-google-sheets/" width="90%" height=500></iframe>

The map pulls the point data and settings from a linked Google Sheet, which you can explore below or right-click to [view full-screen Sheet in a new tab](https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g)
<iframe src="https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g/pubhtml?widget=true&amp;headers=false" width="90%" height=500></iframe>

#### Part 1: Create and customize your map {-}
In the first part of this tutorial, you will learn how to create your own copy of the Leaflet Maps with Google Sheets template, publish your Google Sheet, and paste its web address into your GitHub repo.

- A) Fork (copy) the code template and publish your version with GitHub Pages
- B) File > Make a Copy of Google Sheet template, Share, and File > Publish
- C) Paste your Google Sheet URL in two places in your GitHub repo
- D) Modify your map settings in the Options tab and test your live map

<iframe width="560" height="315" src="https://www.youtube.com/embed/-nGdrzMuUnI?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

#### Part 2: Upload and display your map data {-}
In the second part of this tutorial, you will learn how to geocode and customize your own point markers, and either hide or upload your own polygon and/or polyline GeoJSON data.

- E) Geocode locations and customize new markers in the Points tab
- F) Hide the polygon and polyline legends and default GeoJSON data
- G) Upload and display your own polygon GeoJSON data
- H) Upload and display your own polyline GeoJSON data
- I) Upload and display customized marker icons
- J) Optional: Save Google Sheets as CSV and upload to GitHub
-
** TO DO: second half video**

To solve problems, see [Fix Common GitHub and Code Errors](fix-code) chapter in this book.

#### A) Fork (copy) the code template and publish your version with GitHub Pages {-}

**Before you begin**, this tutorial assumes that you:

- have a [free Google Drive account](http://drive.google.com), and learned the [File > Make a Copy in Google Sheets](copy) tutorial in this book
- have a [free GitHub account](http://github.com), and understand concepts from the [Modify and Host Code with GitHub](github) chapter in this book

1) Right-click to open this GitHub code template in a new tab: https://github.com/datavizforall/leaflet-maps-with-google-sheets

2) In the upper-right corner of the code template, sign in to your free GitHub account

3) In the upper-right corner, click Fork to copy the template (also called a code repository, or repo) into your own account.
The web address (URL) of the new copy in your account will follow this format:
```markdown
https://github.com/USERNAME/leaflet-maps-with-google-sheets
```

Reminder: You can only fork a GitHub repo **one time**. If needed, see how to make a second copy in the [Create a New Repo in GitHub](create-repo) chapter in this book.

4) In your new copy of the code repo, click on Settings, scroll down to the GitHub Pages area, select Master, and Save. This publishes your code to a live map on a public website that you control.

5) Scroll down to GitHub Pages section again, and copy the link to your published web site, which will follow this format:
```markdown
https://USERNAME.github.io/leaflet-maps-with-google-sheets
```

![Screencast](images/13-leaflet/lmwgs-1-fork-640.gif)

6) Scroll up to the top, and click on your repo name to go back to its main page.

7) At the top level of your repo main page, click on README.md, and click the pencil icon to edit this file, written in easy-to-read Markdown code.

8) Delete the link to the current live site, and paste in the link to YOUR site. Scroll down and Commit to save your edits.

9) On your repo main page, right-click the link to your live map to open in a new tab. **Be patient** during busy periods on GitHub, when your website may take up to 1 minute to appear the first time.

#### B) File > Make a Copy of Google Sheet template, Share, and File > Publish {-}

1) Right-click to open this Google Sheets template in a new tab: https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g

2) Sign into your Google account

3) File > Make a Copy of the Google Sheet template to your Google Drive

4) Click the blue Share button, click Advanced, click to change Private to Anyone with the link > Can View the Sheet. This will make your public data easier to view in your map.

![Screencast: Share Google Sheet for anyone with the link to view](images/13-leaflet/lmwgs-2-make-copy-640.gif)

5) File > Publish the Link to your Google Sheet to the public web, so the Leaflet map code can read it.

![Screenshot: File > Publish the link to your Google Sheet](images/13-leaflet/lmwgs-file-publish.png)

6) At the top of your browser, copy your Google Sheet web address or URL (which usually ends in `...XYZ/edit#gid=0`). Do NOT copy the published URL (which usually ends in `...XYZ/pubhtml`).

![Screenshot: Copy the Google Sheet URL, not the Publish URL](images/13-leaflet/lmwgs-copy-sheet-url-not-pub-url.png)

#### C) Paste your Google Sheet URL in two places in your GitHub repo {-}

1) First, connect your Google Sheet directly to your Leaflet Map code. In your Github code repo, click to open this file: `google-doc-url.js`

2) Click the pencil symbol to edit the file.

3) Paste your Google Sheet URL into the code to replace the current URL. Do not delete the single-quotation marks or semicolon.

4) Scroll to bottom of page and press Commit to save your changes. Now the Leaflet Map code can locate your published Google Sheet.

![Screencast: Copy Google Sheet URL and paste into GitHub code](images/13-leaflet/lmwgs-paste-google-sheet.png)

5) Next, let's paste your Google Sheet URL in a second place to keep track of it. Go to the README.md file in your GitHub repo, click to open and edit, and paste your Google Sheet web address to replace the existing link near the top. Commit to save your changes.

#### D) Modify your map settings in the Options tab and test your live map {-}

In the top-level of your GitHub repo, test the new links to your map and your Google Sheet to make sure they work and point to your versions.

** TO DO - redo GIF **

In your linked Google Sheet, go to the Options Tab and modify these items:

1) Map Title -- insert your own title

2) Map Subtitle -- insert your own version

3) Author Name -- insert your own name, or first name, or initials (will be public)

4) Author Email or Website -- insert your own (will be public), or delete the current name to make it blank

Open the link to your live map in a new browser tab and refresh to see your changes.

#### E) Geocode locations and customize new markers in the Points tab {-}

In your new map, our next goal is to add and modify the appearance of a new set of point markers, based on new addresses that you will enter and geocode.

In the Points tab of your Google Sheet:

1) Think of a simple data story that involves at least four geocodeable locations, divided into at least two groups. If you need an example, use this sample table of “Famous Places in New York City”:

| Group     | Name     | Location |
| :-------- | :------- | :------  |
| Landmark  | Empire State Building | 350 5th Ave, New York, NY 10118 |
| Landmark  | Metropolitan Museum of Art | 1000 5th Ave, New York, NY 10028 |
| Transit   | Grand Central Terminal | 89 E 42nd St, New York, NY 10017 |
| Transit   | Penn Station | 159 West 33rd Street, New York, NY 10120 |

2) Enter your Group, Name, and Location data into new rows below the current data.

3) Go to the Font Awesome Icons site, http://fontawesome.io/icons, scroll down to Search Icons, find your desired icon code name, and insert this into the Marker Icon (column B) of your Points sheet. For example, search for and insert the icon code "train" or "building" to display markers with either of these symbols in your map. (To upload your own customized marker, see section H further below.)

4) In Marker Color (column C), use the drop-down menu to select a marker color.

5) In Icon Color (column D), insert a color word (example: white) or hex code (example: #fff) to color the icon symbol inside your marker. Recommended: use white icon colors with dark marker colors.

6) Leave Custom Size (column E) blank.

7) Optional:
  - In Image (column G), insert the URL (preferably https://, not http://) of a small-to-medium sized image on the web
  - In Description (column G), insert text and/or a web link enclosed with an [HTML a href tag with target set to blank](https://www.w3schools.com/tags/tag_a.asp)

8) Do NOT delete or rename any column headers. However, you have the option to add new column headers to display in your map table.

9) Geocode your new data inside your Google Sheet by dragging your cursor to select 6 columns of data: Location - Latitude - Longitude - Found - Quality - Source

10) In the Geocoder menu that appears in this Google Sheet template, select one of the geocoding services. If one service cannot locate your data, try the other. Always inspect the accuracy of the Found column.

Open the link to your live map in a new browser tab and refresh to see your changes. If your new markers appear correctly, then delete the existing rows that came with this template.

#### F) Hide the polygon and polyline legends and default GeoJSON data {-}

To show a simple point map, learn how to turn off and hide the polygon and polyline legend and default data that came with this template. (See how to add your own GeoJSON data in section G below.)

In your linked Google Sheet:

1) In the Options tab, Polyline Legend Position (cell B 35) -- select Off to hide the legend

2) In the Polygons tab, Polygon Legend Position (cell B 4) -- select Off to hide the legend

3) In the Polygons tab, Polygon GeoJSON URL (cell B 6) -- delete contents to remove polygons

4) Go to the next tab, named Polygons1, in its drop-down menu, select Delete to remove sheet

5) In the Polylines tab, delete the entire row (rows 2 and 3) to remove the existing lines

Go to the browser tab with your new map, and refresh the page to see your changes.

Optional:

- in the Options tab, Display Table (cell B 29), turn off to hide the table in your map
- or modify the list of item in Table Columns (cell B 30) to change the display in your table

#### G) Upload and display your own polygon GeoJSON data {-}

1) Prepare your polygon file in GeoJSON format. View or modify the GeoJSON file properties (such as name, data fields, etc.) with one of these tools:

- GeoJSON.io, http://geojson.io -- Drag-and-drop your file, and select the Table tab to view or rename properties. See [GeoJSON.io tutorial](geojsonio) in this book, OR
- MapShaper, http://mapshaper.org -- Drag-and-drop your file. To edit, see [MapShaper tutorial](mapshaper) in this book

2) In your GitHub repo, click to open the Geometry subfolder, then click Upload Files, drag-and-drop your geojson file, and Commit changes

** TO DO ** - turn on settings that you turned off in step F above

3) In your linked Google sheet, go to Polygons tab to adjust these settings:
- change Polygon GeoJSON URL (cell B 6) to match the pathname of the file you uploaded above
- change Polygon GeoJSON Name (cell B 5) to the title to be displayed for this polygon layer
- change Polygon Legend Title (cell B 3) for the title in the polygon legend box

4) To adjust the polygon legend colors and range, see the Polygon Data and Color Settings sections of the Polygon tab in Google Sheets.

5) The code supports multiple polygon layers, which you can add (or delete) by duplicating the Polygons tab. Name them Polygons1, Polygons2, etc.

* TO DO *
-  Explain: To use both the automatic ColorBrewer Palette and manual colors, insert blanks (goes to automatic palette above), separated by semicolons.

#### H) Upload and display your own polyline GeoJSON data {-}

Follow similar steps as described in the Polygon section above, but adjust settings in the Polylines tab of your linked Google Sheet.

#### I) Upload and display customized marker icons {-}

** TO DO **

#### J) Optional: Save Google Sheets as CSV and upload to GitHub {-}

If desired, you can save your table data with your code, rather than in a separate Google Sheet. Go to each Sheet tab and File > Save As in CSV format, with these file names:

- options.csv
- points.csv
- polygons.csv (also: polygons1.csv, polygons2.csv, etc.)
- polylines.csv
- notes.csv  (or .txt)

Upload these files into the main level of your GitHub code repository, where the template will process them automatically.

#### Learn more {-}
To solve problems, see [Fix Common GitHub and Code Errors](fix-code) chapter in this book.
