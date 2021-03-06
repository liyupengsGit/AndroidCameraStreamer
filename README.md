Android Camera Streamer
=======================
Copyright 2011-2012 Andrej Pancik

Android Camera Streamer is a project implementing data streaming (video, gyro, etc.) and processing from Android Phone and computer.

Contents
========

This archive contains a selection of code outputs I created while working on this project. The project tree is organized as follows.

    android/        	directory for java source files for Android
    cpp/            	directory for c++ source files for Mac
	datapacket.proto	protocol buffer specification
    doc/            	directory for documentation
    include/        	header files
	LICENCE.md			licence file
    make.sh         	make script
    matlab/         	directory for mex and Matlab source files
    README.md			this file

Installation
============

A prebuild binaries for 64 bit Mac can be found in the root directory of this arhchive. For simplest rig do

1) Start video host with default settings:

	$ ./videohost

2) Run videostreamer with default settings. This will start 

	$ ./videostreamer
	
3) You should see videohost showing preview window with webcam stream

Compile
=======

To compile Android video streamer application one needs Android SDK (2.3.3) and Android NDK (n7b) installed. In addition, newest OpenCV for Android is required from the trunk (rev 7621). The reason is the recent implementation of imencode for image encoding.

To compile PC/MAC application one needs to have compiled & installed gcc, OpenCV 2.3.1, Protocol Buffers 2.4.1, Boost 1.49.0. For Matlab video host Matlab R2012a with MEX is required.


After compiling and installing all the prerequisites edit make.sh with the path to your OpenCV.

After that run

    $ ./make.sh

to compile.