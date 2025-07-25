# Reality Check
Just for those of you who might be concerned about the Climate Change, here are couple of sobering insights:
- Neil deGrasse Tyson's perspective on climate change: [YouTube Video](https://www.youtube.com/watch?v=tRA2SfSk2Tc)
- My perspective, with statements from two AI entities: [Climate Change](https://githubdragonfly.github.io/viewers/templates/Climate%20Change.txt)

# HTML_CSS_JS
Notes about three.js viewers included in this project:
- all of these viewers should be considered obsolete and are here for historical purposes
- all of these viewers, plus new ones, should be fully functional on the main [webpage](https://githubdragonfly.github.io)
- any future updates and additions will be maintained on the main webpage

Generally intended for educational purposes.

The latest GUI is slightly different than what the screenshot below shows. Also, the preview should show OK on mobile devices as well.

This project features an exercise in HTML, CSS and JavaScript ( [jQuery](https://jquery.com/download/) as well ). Intended for those who either might be learning these or would just like to have several examples in a single page. See the screenshot for what the top part of this page looks like in the Firefox browser (or just use the preview link from the `Usage` section).

For a version with the Flask server, check the [HTML_CSS_JS_Flask](https://github.com/GitHubDragonFly/HTML_CSS_JS_Flask) project. 

Some of these are relatively simple examples and could help you learn these programming languages. Some code was simply adopted and modified from original public sources. There is definitely lots of rotation examples, so try not to get dizzy.

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
 - Links to Wavefront 3D OBJ / Stanford 3D PLY + STL (STereoLithography) / Khronos Group GLTF and DAE (Collada) file viewers, using Three.js found [here](https://threejs.org/) and [here](https://github.com/mrdoob/three.js)
   - some example OBJ / PLY / STL / GLTF files are in the `Images` folder
   - some example DAE files can be found in the [HTML_CSS_JS_Flask](https://github.com/GitHubDragonFly/HTML_CSS_JS_Flask) project's `Images` folder
   - there is far more examples in the [Three.js](https://github.com/mrdoob/three.js) project

## Mozilla Firefox screenshot

Main Menu Page
![Start Page](screenshot/Exercise.png?raw=true)

Some things might not be supported or work as expected on certain browsers. This was tested as working in the latest Firefox and Edge browsers on Windows 10 and Chromium on CloudReady 89.4.0.  The page did also show properly in the TenFourFox browser on MacOS X 10.5 (iMac G5) with the following notes:
 - missing emojis support for old OS X can be compensated, to a degree, with [Symbola Font](https://dn-works.com/ufas/)
 - alignment entries of `float: inline-start` and `float: inline-end` did not work and needed to be replaced with `float: left` and `float: right`, which works for modern browsers as well and has now been standardized in this exercise
 - add-on required to provide support for [playing MP4 video](https://sourceforge.net/projects/tenfourfox/files/addons/mp4/1.3406/) in TenFourFox
 - no camera video recording could be done since TenFourFox doesn't support async/await. Even with a different code, it also seems to be having difficulties with `video.captureStream` (the Blob is created but its size is always 0 bytes)
 - OBJ and PLY viewers did not work due to poor WebGL support (blacklisting)

It would be recommended that you also check [this project](https://github.com/GitHubDragonFly/WebProject) and look at all the files created by it, especially because it is interacting with the django built-in server (there is also a link to django tutorial).

## Notes:
 - Camera "Id" feature is experimental and was not tested against multiple cameras.
 - Camera "Record" feature is experimental and seems to be working properly (if needed, modify and use the best you can):
   - It depends on the browser supporting ".webm" media format (HTML5)
   - The "Save" link should turn green to offer to "download" and save the recorded video (no actual downloading from any external website is done, this is all on your computer)
 - Adding more information to inline frame (iFrame) - you can get instructions for obtaining info about your browser and your public IP by visiting [WhatIsMyBrowser](https://www.whatismybrowser.com/developers/tools/iframe) developers page.
 - "3D Cube 1" drawing code might eventually need some corrections. Currently, the transparency allows it to be seen as correct but if you go about changing the "fill" and "stroke" values to more solid, 0.1 changed to 1.0, then you might see somewhat incorrect transitions. This is even more obvious if painting each side of the cube with a different color.
 - OBJ, PLY + STL, GLTF and DAE Viewers:
   - All viewers require a browser supporting WebGL and are set to open in the new tab/window
   - GLTF and DAE viewers are set to use Orbit Controls while other viewers do allow some mouse control, with `wheel` being zoom in/out and `left-button click/drag` rotating the image
   - Scene background image supported formats are PNG, JPEG, SVG, BMP and GIF while selecting non-image file will reset the background
   - Either a local OBJ file alone or MTL + OBJ files or MTL + OBJ + JPG / PNG / BMP / GIF files or MTL + OBJ + DDS files can be loaded at the dialog screen
   - If the MTL file requires texture files then you have to select and load them, otherwise check the console output for errors
   - Either a local PLY file alone or PLY + JPG / PNG / BMP / GIF texture files can be loaded at the dialog screen (texture files should be relatively simple)
   - A local STL file should be loaded alone since it doesn't play well with textures
   - Either a local GLB / GLTF file alone or GLB / GLTF + JPG / PNG / BMP / GIF files can be loaded at the dialog screen
   - Either a local DAE file alone or DAE + JPG / PNG / BMP / GIF / DDS files can be loaded at the dialog screen
   - GLTF / DAE viewers also have a URL option available, which should fetch all associated resources and is probably the best choice
   - GLTF / DAE viewers currently support animations (some example GLB files are animated)
   - GLTF / DAE viewers currently don't support local loading of .bin files (use URL option instead to fetch all the resources)
   - GLTF viewer currently doesn't support DRACO or KTX2 loading while these are available in the [HTML_CSS_JS_Flask](https://github.com/GitHubDragonFly/HTML_CSS_JS_Flask) project 
   - GUI has lights marked as DL, SL, HL and AL (directional, spot, hemisphere and ambient)
   - All viewers allow changing the XYZ positions of DL / SL / HL lights, swappable with `Rotate`
   - The DLi / SLi control those lights intensity
   - The SpotLight is set to cast a shadow so use it for anything shadow related
   - The material of the object is set to cast but not receive the shadow
   - Additional plane receiving shadow is set in the background, controlled by the `Shadow` checkbox, the SpotLight intensity and the opacity of the object
   - Most of the OBJ / PLY / GLTF examples were downloaded from [here](https://github.com/mrdoob/three.js)
   - My own OBJ, STL and PLY examples were created simply by using online services to perform conversion from PNG to STL, STL to OBJ and then OBJ to PLY ([Blender](https://www.blender.org/) was also used to decrease the size of the files and add MTL with some shading to OBJ example)
   - There are screenshots of most viewers, each showcasing one of the mentioned examples, shadow enabled
 - Alternative software viewers/editors, which support more than just OBJ / PLY / GLTF formats:
   - Three.js [editor](https://threejs.org/editor/) available online
   - [Online 3D Viewer](https://github.com/kovacsv/Online3DViewer)
   - Windows 10 users have an option to use `Paint 3D` and `3D Viewer` apps

# Usage
All it takes is to try either of the following:

- Thanks to the [GitHub & BitBucket HTML Preview](https://github.com/htmlpreview/htmlpreview.github.com) you can preview the [Exercise](https://htmlpreview.github.io/?https://github.com/GitHubDragonFly/HTML_CSS_JS/blob/main/Files/Exercise.html) page and use its fixed menu to access the rest (jQuery section might not work with this preview). This was tested as working in the Firefox browser and you could optionally use ctrl+click to open it in the new tab/window.

And just for the convenience, you can access the viewers directly here: [OBJ](https://htmlpreview.github.io/?https://github.com/GitHubDragonFly/HTML_CSS_JS/blob/main/Files/OBJ%20Viewer.html) / [PLY + STL](https://htmlpreview.github.io/?https://github.com/GitHubDragonFly/HTML_CSS_JS/blob/main/Files/PLY%20Viewer.html) / [DAE](https://htmlpreview.github.io/?https://github.com/GitHubDragonFly/HTML_CSS_JS/blob/main/Files/DAE%20Viewer.html) / [GLTF](https://htmlpreview.github.io/?https://github.com/GitHubDragonFly/HTML_CSS_JS/blob/main/Files/GLTF%20Viewer.html)

OR do it this way:

- Download a zip file of this project and extract it (or clone the repo) - this will help with having local example files available for loading.
- Navigate to the `Files` folder and open `Exercise.html` in your Internet browser.
- The `Exercise.html` is serving as a hub but any of the HTML files can be open in the browser on its own
- If any change is required then try using VS Code or Notepad to edit files.

# Licensing
This is MIT licensed.

Three.js MIT license is included in the `js` folder together with a link to jQuery MIT license.
Some files/examples obtained from the three.js project might have a note included about their own license.

The beach video and the cube/die image were downloaded as a free media content and are under the [Pixabay License](https://pixabay.com/service/license/).

# Trademarks
Any and all trademarks, either directly or indirectly mentioned here, belong to their respective owners.

# Resources
All of the ones I used are in the REFERENCES.md file and whatever other resources you can find.

Some additional resources, for creating your own OBJ / PLY files, are in the README.md files inside `Images/obj/dragonfly` and/or `Images/ply/ascii` folders.
