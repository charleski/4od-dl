4od-dl
======

Ruby script to download, convert and tag stuff from 4od.

Supported Platforms
===================

This script has been tested on OS X 10.7 (Lion). I imagine it will work on older versions of OS X and perhaps on Linux too, but I've not tested it. 

It definitely won't run on Windows but other than the hardcoded 'which' calls to find rtmpdump/ffmpeg/AtomicParsley it should probably work. Feel free to have a go and send a pull request :).  

Pre-Requisites
=========

To run, the following 3 binaries must be resolvable via your PATH:

1. rtmpdump: Either [download and compile yourself](http://rtmpdump.mplayerhq.hu/) or grab the OS X package from [trick77.com](http://trick77.com/2011/07/30/rtmpdump-2-4-binaries-for-os-x-10-7-lion)
2. ffmpeg: Either [download and compile](http://ffmpeg.org/) or grab the OS X binary from [ffmpegmac.net](http://ffmpegmac.net)
3. AtomicParsley: Either download and compile or grab the binary from [atomicparsley.sourceforge.net](http://atomicparsley.sourceforge.net/)

It also uses the following gems that you must install (I will sort out a Gemfile eventually):

* logger
* hpricot
* crypt

Usage
=====

	Usage: 4od-dl [options]
    	-p, --programids ID1,ID2,ID3     Program IDs to download - this is the 7 digit program ID that you find after the hash in the URL (e.g. 3333316)
    	-o, --outdir PATH                Directory to save files to (default = pwd)

For instance the ID for the following programme is 3264880: http://www.channel4.com/programmes/grand-designs/4od#3264880

To Do
======

This is a pretty rough hack so I'd like to add (in no order):

* Basic text-based PVR functionality to find programmes to download
* More control over the filename
* Use a Gemfile to manage Gem dependencies
* ~~Ability to download to another directory than the one you're running 4od-dl in~~ **Done 14th May**
* ~~Remove the .flv once downloading is complete~~ **Done 14th May**

