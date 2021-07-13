# HTML_CSS_JS
Exercise in HTML, CSS and JavaScript ( [jQuery](https://jquery.com/download/) as well ). Intended for those who either might be learning these or would just like to have several examples in a single page. See the screenshot for what the top part of this page looks like in the Firefox browser.

Some might consider these as relatively simple examples but they only reflect a way of how I am going about learning these languages. Some code was simply adopted and modified from original public sources. There is definitely lots of rotation examples, so try not to get dizzy.

A good portion of the page should be self-explanatory, some content is static, some animated and some is interactive.

These are the features you can see on the page:
 - Bookmark style menu bar fixed on top of the page and footer on the bottom
 - Mix of internal and inline CSS styling (move it to external styles.css file if needed)
 - Basic stuff, like headers, lists, tables and mixed inline text of different colors and sizes
 - Rotating over X, Y, Z, XY, XZ, YZ, XYZ axes as well as drawing and rotating SVG
 - Inline frame (iframe) with several pages, tabbed browsing and 3D cubes
 - Form and submitted form entries table (there is no server involved in this exercise)
 - Media video playback, including camera streaming and an option to record and save the camera video
 - JavaScript and jQuery examples
 - Link to Wavefront 3D OBJ file viewer, using [Three.js](https://github.com/mrdoob/three.js) (some example OBJ files are in the `Images/obj` folder)
 - Link to 3D PLY file viewer, using [Three.js](https://github.com/mrdoob/three.js) (some example PLY files are in the `Images/ply` folder)

Some things might not be supported or work as expected on certain browsers. This was tested as working in the latest Firefox and Edge browsers on Windows 10 and Chromium on CloudReady 89.4.0.  The page did also show properly in the TenFourFox browser on MacOS X 10.5 (iMac G5) with the following notes:
 - missing emojis support for old OS X can be compensated, to a degree, with [Symbola Font](https://dn-works.com/ufas/)
 - alignment entries of `float: inline-start` and `float: inline-end` don't work and need to be replaced with `float: left` and `float: right`, which works for modern browsers as well and has now been standardized in this exercise
 - add-on required to provide support for [playing MP4 video](https://sourceforge.net/projects/tenfourfox/files/addons/mp4/1.3406/) in TenFourFox
 - no camera video recording could be done since TenFourFox doesn't support async/await. Even with a different code, it also seems to be having difficulties with `video.captureStream` (the Blob is created but its size is always 0 bytes)
 - OBJ and PLY viewers did not work due to poor WebGL support

It would be recommended that you also check [this project](https://github.com/GitHubDragonFly/WebProject) and look at all the files created by it, especially because it is interacting with the django built-in server (there is also a link to django tutorial).

## Notes:
 - Camera "Id" feature is experimental and was not tested against multiple cameras.
 - Camera "Record" feature is experimental and seems to be working properly (if needed, modify and use the best you can):
   - It depends on the browser supporting ".webm" media format (HTML5)
   - The "Save" link should turn green to offer to "download" and save the recorded video (no actual downloading from any external website is done, this is all on your computer)
 - Adding more information to inline frame (iFrame) - you can get instructions for obtaining info about your browser and your public IP by visiting [WhatIsMyBrowser](https://www.whatismybrowser.com/developers/tools/iframe) developers page.
 - "3D Cube 1" drawing code might eventually need some corrections. Currently, the transparency allows it to be seen as correct but if you go about changing the "fill" and "stroke" values to more solid, 0.1 changed to 1.0, then you might see somewhat incorrect transitions. This is even more obvious if painting each side of the cube with a different color.
 - OBJ and PLY Viewers notes:
   - Both viewers require a browser supporting WebGL and are set to open in new tab/window
   - They do allow some mouse control, with `wheel` serving as zoom in/out and `left-button click/drag` to rotate the image
   - Either an OBJ file alone or both MTL/OBJ files can be loaded at the dialog screen
   - Only a PLY file alone can be loaded at the dialog screen
   - OBJ and PLY examples were downloaded from [here](https://github.com/mrdoob/three.js)

# Usage
All it takes is to:

- Download a zip file of this project and extract it (or clone the repo).
- Navigate to the `Files` folder and open `Exercise.html` in your Internet browser.
- If any change is required then try using VS Code or Notepad to edit files.

# Licensing
This is MIT licensed.

The beach video and the cube/die image were downloaded as a free media content and are under the [Pixabay License](https://pixabay.com/service/license/).

# Trademarks
Any and all trademarks, either directly or indirectly mentioned here, belong to their respective owners.

# Resources
All of the ones I used are in the REFERENCES.md file and whatever other resources you can find.
