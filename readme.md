# Neptune Computational Biology - Final Project

# Working with cell tracking data

## Introduction and Goals

The goal of my project is to work with positional data obtained from migrating and dividing nuclei (x, y, z, coordinates), which are called trajectories. The data was obtained from live imaging movies of a developing embryo. One challenge is that the trajectories are non-continous, mostly for two reasons. Firstly some nuclei are lost during the detection with the algorithm and secondly the alorithm that detects nuclei has to be adjusted to the dynamics of the developing embyo (e.g. change in nuclei size). It will be very useful for me to find a way how to stich broken trajectories together.

The first step of this project is to generate cell tracking data from a movie. The I will use python to open and read .xls files that were produced with Trackmate and contain the trajectory information. Tracks will be re-saved as individual text files. After this pre-processing step the data will be available for further processing.

The data I will use are my own data data and come from OpenSPIM live imaging movies on which nuclei can be traced. For nuclear detection and tracing the Fiji plugin Trackmate was used on a very short test movie to create a small test data set.

## Methods

The original z-stack used for this project can be downloaded [here](https://www.dropbox.com/s/shb3zdfc6q9id08/H2AmCh-341x341.tif?dl=0) (170 MB):
To better understand the original data a maximum z-projection of the movie in from of an .avi file can be seen [here](https://www.dropbox.com/s/c3pf76fmdoftlvv/H2AmCh-341x341_MAX_colored.avi?dl=0). 

Single particle tracking was performed with the [Fiji](http://fiji.sc/) plugin [Trackmate](http://imagej.net/TrackMate) to obtain nuclear position and resulted in the following two tables.
	
	- Links.xls
	- Spots.xls

I will use Python code with regular expressions to open, modify and extract track number and the nuclear positon of the trajectories.

A dictionary was created to make data handling more flexible and allows to gain info such as:
	
	- Track lengths
	
	- resaving as individual track*.txt files


The tools I used were... See analysis files at (links to analysis files).

## Results

![Figure 1](./Figure1.png?raw=true)

In Figure 1...

## Discussion

These results indicate...

The biggest difficulty in implementing these analyses was...

If I did these analyses again, I would...

## References


