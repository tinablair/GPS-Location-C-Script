GPS Location in Unity 2020 
\`[YouTube video](https://www.youtube.com/watch?v=JWccDbm69Cg)`\
Posted on YouTube by Code 3 Interactive
------------------------------------------------------------------------------------------------------
The following instructions written by Tina Blair
\`[Email Me](mailto:tina.web.developer@gmail.com)` *Not intended for beginners*
------------------------------------------------------------------------------------------------------
```
((Note: Please view the following steps in the Game window.))
```
```
In Unity:
  * GameObject > UI > EventSystem
  * Create GPSLocation gameobject in the Hierarchy
  * Add the script to this GPSLocation gameobject
```
```
  Now you can see the parameters from the code in the Inspector window:
    GPS Status
    Latitude Value
    Longitude Value
    Altitude Value
    Horizontal Accuracy Value
    Timestamp Value
```
```
In Unity:
  GameObject > UI > Text

  In the Hierarchy, select Canvas

  In the Inspector, change the Reference Resolution and Match values
    * (In the YouTube video referenced on line 1, they change the
      Reference Resolution to X 1920 Y 1080 and Match to 0.5)

  In the Hierarchy, select Text (child of Canvas) and change the
    Font Size if needed
    * (In the YT video, they change the Font Size to 70 and add Bold)

  In the Inspector, change the Width and Height of the Rect Transform
    * (In the YT video, they change the Width to about 460 and the
      Height to about 161)
    * Change the text to say: GPS Location 
    * Centre the text under Rect Transform (Centre Top)
    * Change Pos Y to -191

  In the Hierarchy, duplicate the Text gameobject
    * Rename Text to Title
    * Rename Text(1) to GPSStatus
      * Change Pos X -146.7 Pos Y -318
      * Change Text to read "GPS Location:" (Inspector under Text) and
        Font Size 50

  In Hierarchy:
    * Duplicate GPSStatus
    * Rename GPSStatus(1) to latitude
    * Change Text to read "Latitude:" (Inspector under Text)

  In Hierarchy:
    * Duplicate latitude and rename longitude
    * Change Text to read "Longitude:" (Inspector under Text)

  In Hierarchy:
    * Duplicate longitude and rename altitude
    * Change Text to read "Altitude:" (Inspector under Text)

  In Hierarchy:
    * Duplicate altitude and rename HorizontalAccuracy
    * Change Text to read "Horizontal Accuracy:" (Inspector under Text)

  In Hierarchy:
    * Duplicate HorizontalAccuracy and rename timestamp
    * Change Text to read "Timestamp:" (Inspector under Text)

  In Hierarchy:
    * Duplicate GPSStatus -> Timestamp (and all in between - 6 in total)

  Place the text of these newly duplicated gameobjects in line with the
    same name. Like this:

    GPSStatus:            GPSStatus:
    Latitude:             Latitude:
    Longitude:            Longitude:
    Altitude:             Altitude:
    Horizontal Accuracy:  Horizontal Accuracy:
    Timestamp:            Timestamp:

  In Hierarchy:
    * Select GPSStatus(1) -> Timestamp(1) - 6 in total
    * Change the Text to 00
    * Rename as follows (in Hierarchy):
      * GPSStatus(1) to GPSStatusValue
      * latitude(1) to latitudeValue
      * longitude(1) to longitudeValue
      * altitude(1) to altitudeValue
      * HorizontalAccuracy(1) to HorizontalAccuracyValue
      * Timestamp(1) to TimestampValue

  In Hierarchy:
    * Select GPSLocation
      * Drag GPSStatusValue to GPS Status field in the
        GPS Location (Script) component.
    * Select latitude
      * Drag latitudeValue to Latitude Value field in the
        GPS Location (Script) component.
    * Select longitude
      * Drag longitudeValue to Longitude Value field in the
        GPS Location (Script) component.
    * Select altitude
      * Drag altitudeValue to Altitude Value field in the
        GPS Location (Script) component.
    * Select HorizontalAccuracy
      * Drag HorizontalAccuracyValue to Horizontal Accuracy Value
        field in the GPS Location (Script) component.
    * Select Timestamp
      * Drag TimestampValue to Timestamp Value field in the
        GPS Location (Script) component.
```
```
* GameObject (top menu) > UI > Image
* In Hierarchy, select Image and change colour to very light grey
* In Inspector, change Pos X 0 Pos Y -148 Pos Z 0 Width 1143 Height 100 
* In Hierarchy, rename Image to TitleBG and move to the position above
  Title (to place the image *behind* the title "GPS Location" showing in
  the Game window).
* In Hierarchy, duplicate TitleBG and rename FooterBG and leave it at the
  bottom of the list of game objects.
* In Inspector, with FooterBG selected (Hierarchy), change Rect Transform
  Pos Y to 58.8 and Height to 57 (Width may be about 1142.9 so the FooterBG
  goes from left edge to right edge)
* In Hierarchy, duplicate "longitude" game object and rename Footer
```
```
In Inspector, modify Rect Transform:
  * Anchor Preset centre bottom
  * Pos X 0 Pos Y 0.4000244 Pos Z 0
  * Under Text: enter text "www.Code3Interactive.com" (or your own URL)
  * Width 683.6 Height 161.4 (less or more as needed to see all the text)
```
```
In Inspector, modify Text:
  * Font Size 40
  * Paragraph centre top (and any other modifications you prefer)
```
```
In Hierarchy, select GPSStatusValue game object.
```
```
In Inspector under Text, type "Stop"
```
```
File > Build Settings > Player Settings

In the Project Settings window, locate Location Usage Description* 
  (This will give the user how and why you are using location service)

Type: "Location is used for AR asset placement and height analysis, ensuring
       clear image perception. No data is stored/shared with third parties."

(or something like that... while Android does not indicate a limit,
 Apple iOS indicates no more than 150 characters to ensure the message is 
 concise and fits well within the permission dialog box.)
```
