# Skip-Songs-just-with-Looking
skip songs by just looking at music notes

I thought pressing a button or touching a touchscreen to skip songs is too much work ;)
What if you can skip songs by just looking at music notes?

the technique could be applied to a whole range of home automation tasks with some minor tweaks.

In this project I used a Raspberry Pi 3 B+ , a Pi camera , a speaker and a mp3 player.
The operating system was Raspbian and I used OpenCV for image processing.

OpenCV (Open Source Computer Vision Library) is an open source computer vision and machine learning software library.
OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in the commercial products.

The way image recognition works is we first need to "train" a classifier.

To do this, we generally need to compile a massive set of images of what we're looking to detect (In this case face). 
For a lot of the image recognition tasks, people have already built data sets to use for the training part.
Face Detection is very popular, so there are already a lot of datasets for face data (face_p.xml for this project).

After training it checks if face is at the frame or not. if answer is yes it sets GPIO14 to LOW.
GPIO14 attached to skip button in mp3 player (in most of the mp3 players pressing button sets the pin to LOW).

( I used mp3 player to control it with GPIO. so if some one else want to use this code for controlling something else they can easily do it. )
and I attached a LED to GPIO 15 and it turns on for 1 second when there is a face in the frame.

YouTube Video: https://youtu.be/ojnZvVBBWRA
