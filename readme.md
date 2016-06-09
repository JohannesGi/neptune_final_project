# Neptune Computational Biology - Final Project

# Working with cell tracking data

## Introduction and Goals

The goal of my project is to work with positional data obtained from migrating and dividing nuclei (x, y, z, coordinates), which are called trajectories. The data was obtained from live imaging movies of a developing embryo. One challenge is that the trajectories are non-continous, mostly for two reasons. Firstly some nuclei are lost during the detection with the algorithm and secondly the alorithm that detects nuclei has to be adjusted to the dynamics of the developing embyo (e.g. change in nuclei size). It will be very useful for me to find a way how to stich broken trajectories together.

The first step of this project is to generate cell tracking data from a movie. The I will use python or the shell to open and read text files that contain the trajectory information. Then I will isolate and filter the positional information (coordinates). After this pre-processing step the data will be available for further processing.

The data I will use are my own data data and come from OpenSPIM live imaging movies on which nuclei can be traced. For nuclear detection a gradient vector diffusion algorithm proposed by Li et al. 2007 was used. Additionally I will use the Fiji plugin Trackmate on a very short test movie to create my own small test data set.

## Methods

I will use Python code with regular expressions to open, modify and extract track number and the nuclear positon of the trajectories. The code should allow me to select for the best trajectories and discard badly detected trajectories.

The tools I used were... See analysis files at (links to analysis files).

## Results

![Figure 1](./Figure1.png?raw=true)

In Figure 1...

## Discussion

These results indicate...

The biggest difficulty in implementing these analyses was...

If I did these analyses again, I would...

## References


