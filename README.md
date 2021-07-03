# HTML_CSS_JS
Exercise in HTML, CSS and JavaScript ([jQuery](https://jquery.com/download/) as well). Intended for those who either might be learning these or would just like to have several examples in a single page. There is definitely lots of rotation examples, so try not to get dizzy.

Some might consider these as relatively simple examples but they only reflect a way of how I am going about learning these languages. Some code was simply adopted and modified from original public sources.

A good portion of the page should be self-explanatory, some content is static, some animated and some is interactive.

It is using a mix of internal and inline CSS styling, which can always be changed, packed and moved to external styles.css file.

Some things might not be supported or work as expected on certain browsers. This was tested as working in the latest Firefox browser on Windows 10 computer and the page did also show properly in the TenFourFox browser on Power Macintosh with the following notes:
 - missing emojis support for old OS X can be compensated, to a degree, with [Symbola Font](https://dn-works.com/ufas/)
 - alignment entries of "float: inline-start" and "float: inline-end" don't work and need to be replaced with "float: left" and "float: right", which works for modern browsers as well and has now been standardized in this exercise
 - add-on providing support for [playing MP4 video](https://sourceforge.net/projects/tenfourfox/files/addons/mp4/1.3406/) in TenFourFox

It would be recommended that you also check [this project](https://github.com/GitHubDragonFly/WebProject) and look at all the files created by it, especially because it is interacting with the django built-in server (there is also a link to django tutorial).

## Notes:
 - Camera "Id" feature is experimental and was not tested against multiple cameras.
 - Camera "Record" feature is experimental, so modify and use the best you can:
   - It depends on the browser supporting ".webm" media format
   - The "Save" link should turn green to offer to "download" and save the recorded video (no actual downloading from any external website is done, this is all on your computer)
 - Adding more information to inline frame (iFrame) - you can get instructions for obtaining info about your browser and your public IP by visiting [WhatIsMyBrowser](https://www.whatismybrowser.com/developers/tools/iframe) developers page.
 - "3D Cube 1" drawing code might eventually need some corrections. Currently, the transparency allows it to be seen as correct but if you go about changing the "fill" and "stroke" values to more solid, 0.1 changed to 1.0, then you might see somewhat incorrect transitions. This is even more obvious if painting each side of the cube with a different color. 

# Usage
All it takes is to:

- Download a zip file of this project and extract it.
- Navigate to the `Files` folder and open `Exercise.html` in your Internet browser.

# Licensing
This is MIT licensed.

The beach video and the cube/dice image were downloaded as a free media content and are under the [Pixabay License](https://pixabay.com/service/license/).

# Trademarks
Any and all trademarks, either directly or indirectly mentioned here, belong to their respective owners.

# Resources
All of the following that I have used and whatever other resources you can find:

- https://www.w3schools.com
- https://developer.mozilla.org/en-US/docs/Web/API
- https://www.geeksforgeeks.org/how-to-create-a-link-in-javascript/
- https://css-tricks.com/use-and-reuse-everything-in-svg-even-animations/
- https://flaviocopes.com/rotate-image
- https://www.lipsum.com
- https://svgstudio.com/pages/free-sample
- https://stackoverflow.com/questions/11197671/
- https://pixabay.com
- https://codepen.io/MRokas/pen/aNBjdQ
- https://www.sitepoint.com/building-3d-engine-javascript/
- https://codepen.io/desandro/pen/KRWjzm
- https://codepen.io/thiagobraga/pen/bhDdn
- https://mkyong.com/jquery/how-to-use-css-and-jquery-to-hide-and-show-tab-content/
- https://www.kirupa.com/html5/accessing_your_webcam_in_html5.htm
