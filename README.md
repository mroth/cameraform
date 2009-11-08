CameraForm
==========
Attempt at creating an open source library for webcam capture of a static image that gets submitted via a form.  It should support the easy embedding of a capture frame into a HTML form with other parameters.

The idea being that developers wont have to mess around with evil Flash/AS themselves, and instead can download a handy precompiled library that they just interact with via HTML/JS land. 

Obviously what would be more ideal would be browser support for [`<input type=camera>`](http://ajaxian.com/archives/input-camera) but that was apparently nixed from the HTML5 spec, so for now, this.

This is forked from 
* Adding support for getting back the JPEG as a base64 encoded string, so you can submit it via a standard HTML form after you insert the value via Javascript.  This makes it much more flexible for usage in web apps.
* Putting it on github, since github is awesome and allows for easier collaboration.
