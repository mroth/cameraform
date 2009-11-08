CHANGES
This was originally based on jpegcamera by Joseph Huckaby:
http://code.google.com/p/jpegcam/

The following has been modified:
  * added as3base64 library
  * added dump method to return base64 encode jpeg as a string for callback

I used a demo version of Flash CS4 to compile this, and it converted the project file to a CS4 file when I added the .swc to the class library.  I'm not sure how to do that in a way that is compatible with CS3 project files...

ORIGINAL BUILDING INSTRUCTIONS

This library requires the AS3 Core Library (as3corelib) available from Google Code:
	http://code.google.com/p/as3corelib/

After downloading and extracting the package, place the "com" directory right here,
alongside the "Webcam.fla" and "Webcam.as" files.

You should then be able to compile the FLA into a SWF.
This requires Adobe Flash CS3 (this is a Flash 9 movie).
