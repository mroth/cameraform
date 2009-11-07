CameraForm
==========
Attempt at creating an open source library for webcam capture of a static image that gets submitted via a form.  It should support the easy embedding of a capture frame into a HTML form with other parameters.

The idea being that developers wont have to mess around with evil Flash/AS themselves, and instead can download a handy precompiled library that they just interact with via HTML/JS land. 

Obviously what would be more ideal would be browser support for [`<input type=camera>`](http://ajaxian.com/archives/input-camera) but that was apparently nixed from the HTML5 spec, so for now, this.

Functional Spec
---------------
1. Instantiate.
1. Capture.
1. Recapture / Submit.
1. ExternalInterface hooks for JS control.

Parameters
----------
Parameters that should be able to be passed from the HTML instantiation.

* `size(w=320,h=240)`
  The size of the Camera portal.
* `capture_size(w=320,h=240)`
  The size of the resulting image to be stored.
* `countdown(boolean=true)`
  Whether or not to have a 3,2,1 countdown before capture.
* `show_buttons(boolean=true)`
  Whether or not to have visible capture buttons in the frame.
