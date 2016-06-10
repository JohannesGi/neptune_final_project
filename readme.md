# Neptune Computational Biology - Final Project

# Working with cell tracking data

## Introduction and Goals

The goal of my project is to work with positional data obtained from migrating and dividing nuclei (x, y, z, coordinates), which are called trajectories. The data was obtained from live imaging movies of a developing embryo. One challenge is that the trajectories are non-continous, mostly for two reasons. Firstly some nuclei are lost during the detection with the algorithm and secondly the alorithm that detects nuclei has to be adjusted to the dynamics of the developing embyo (e.g. change in nuclei size). It will be very useful for me to find a way how to stich broken trajectories together.

The first step of this project is to generate cell tracking data from a movie. The I will use python to open and read .xls files that were produced with Trackmate and contain the trajectory information. Tracks will be re-saved as individual text files. After this pre-processing step the data will be available for further processing.

The data I will use are my own data data and come from OpenSPIM live imaging movies on which nuclei can be traced. For nuclear detection and tracing the Fiji plugin Trackmate was used on a very short test movie to create a small test data set.

## Methods & Results

The original z-stack used for this project can be downloaded [here](https://www.dropbox.com/s/shb3zdfc6q9id08/H2AmCh-341x341.tif?dl=0) (170 MB).
To better understand the original data a maximum z-projection of the movie in from of an .avi file can be seen [here](https://www.dropbox.com/s/c3pf76fmdoftlvv/H2AmCh-341x341_MAX_colored.avi?dl=0). 

Single particle tracking was performed with the [Fiji](http://fiji.sc/) plugin [Trackmate](http://imagej.net/TrackMate) to obtain nuclear position, which is saved into the table [Spots.xls](https://github.com/JohannesGi/neptune_final_project/blob/master/Data/Trackmate/original-data/Spots.xls).
	
Two Python scripts were written to extract x,y,z coordinates (given in µm) and corresponding tracknames.
 	
 	1.) Initially the script "track_extractor" uses the following regular expressions (re):
 	'^\d+\t[(+*)]\w.*[(+*)]\t(\d+)\t\d+\t\d+\t\d+\.\d+\t\d+\.\d+\t(\d+\.\d+)\t(\d+\.\d+)\t(\d+\.\d+).+'.

 	2.) Secondly the script dict_track_extractor_spots was written. The script uses a simple Line.split command
 	to access x,y,z and tracknames. Additionally this code creates a dictionary, which allows to take each track
 	separatly containing all nuclear positions and resaves them as individual .txt files, for example track5.txt

 To quickly check for the total amount of tracks and their individual track lengths the python script 'track_analyser' can be used on any generated Spot.xls files.

Each individual track*.txt file can be importet with the python script 'track-viewer', which will generate a 3-dimensional plot showing all nuclear positions at once. To do this the [matplotlib](http://matplotlib.org/index.html) has to be [installed](http://matplotlib.org/users/installing.html).


The following figures ([Figure1](https://github.com/JohannesGi/neptune_final_project/blob/master/figure_1_track3.png), [Figure2](https://github.com/JohannesGi/neptune_final_project/blob/master/figure_2_track7.png), [Figure3](https://github.com/JohannesGi/neptune_final_project/blob/master/figure_4_track16.png), [Figure3](https://github.com/JohannesGi/neptune_final_project/blob/master/figure_3_track13.png)) show examples of different tracks visualized with 'track-viewer'.
Figure 1-3 represent the dynamics of nuclear positions during imaging.


Figure1 - Track3                                   |  Figure2 - Track7
:-------------------------------------------------:|:--------------------------------------------------:
![Figure 1](./figure_1_track3.png?raw=true)        |  ![Figure 2](./figure_2_track7.png?raw=true)

Figure3 - Track13                                  |  Figure4 - Track16
:-------------------------------------------------:|:--------------------------------------------------:
![Figure 3](./figure_3_track13.png?raw=true)       |  ![Figure 4](./figure_4_track16.png?raw=true)


## Discussion

These results indicate...

The biggest difficulty in implementing these analyses was...

If I did these analyses again, I would...

## References


