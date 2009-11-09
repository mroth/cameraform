CameraForm
==========
Attempt at creating an open source Flash+Javascript library for webcam capture of a static image that gets submitted via a form.  It should support the easy embedding of a capture frame into a HTML form with other parameters.

The idea being that developers wont have to mess around with evil Flash/AS themselves, and instead can download a handy precompiled library that they just interact with via HTML/JS land. 

Obviously what would be more ideal would be browser support for [`<input type=camera>`](http://ajaxian.com/archives/input-camera) but that was apparently nixed from the HTML5 spec, so for now, this!


Differences from jpegcam
------------------------
This project is forked from [jpegcam](http://code.google.com/p/jpegcam/) (v1.08) by jhuckaby.  The notable changes are:

* Adding support for getting back the JPEG as a base64 encoded string, so you can submit it via a standard HTML form after you insert the value via Javascript.  This makes it much more flexible for usage in web apps, and is consistent with the goal of doing as little in Flash as possible.
* TODO: Adding `console.log` calls via ExternalInterface in addition to `trace()`, for ease of debugging in web browser with Firebug.
* Putting it on github, since git and github are awesome and allow for easier collaboration.

As per the parent project, it is licensed under LGPL license terms.

Usage
-----
For now, look at the [jpegcam documentation](http://code.google.com/p/jpegcam/wiki/Instructions) for basic setup stuff.

*The main difference here is that once you `freeze()` the image, instead of calling `upload()`, you can call `dump()` instead, which will return a base64 encoded JPEG to the callback handler.*

Once you get the return value in the callback, you can just stick it in a hidden form value:
	
	<form onSubmit='doSomething();'>
		<!-- your other form stuff here -->
		<input type='hidden' id='img_data'>
		<input type='submit' id='submit_button' disabled='true'>
	</form>
	<script language="JavaScript">
		webcam.set_hook( 'onComplete', 'completion_handler' );
	
		function completion_handler(data) {
			document.getElementById('img_data').value = data;
			document.getElementById('submit_button').disabled = false;
		}
	</script>

I'm assuming you already know what to do with a form!

You can even preview it by writing a data-uri into the src of an image.  Assuming we have an image with `id=preview`, then:

	var p = document.getElementById('preview');
	p.src = 'data:image/jpeg;base64,' + data;

Fun for the whole family.

Demo
----
Probably easiest to just look at the source code on [the demo page](http://mroth.github.com/cameraform/htdocs/test.html).

License
-------
LGPL
