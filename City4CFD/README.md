# Automatic 3D model reconstruction 

City4CFD --City for CFD-- is an automated tool for generating 3D city models optimized 
for microscale urban flow simulations. The open-source can be found: 

https://github.com/tudelft3d/City4CFD
CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Requirements
 * Implementation
 

INTRODUCTION
------------
The 3D Geo-information Research Group at Delft University of Technology has developed an
open-source software called City4CFD. This software is designed to automatically create 
3D city models suitable for use in micro-scale computational wind engineering simulations.


REQUIREMENTS
------------
To successfully run City4CFD, the following inputs are required:

	1. Building footprints in GeoJSON format
	2. Polygons of vegetation, water, and roads in GeoJSON format
	3. Point cloud data

It is important to ensure that the point cloud and GeoJSON files are in the same coordinate system.


IMPLEMENTATION
-------------
After installing the open-source software City4CFD on your computer by following the steps mentioned on
the corresponding GitHub page, it is an easy task to automatically reconstruct the 3D model in LOD1.2 
by following the next set of commands:

	cd examples/
	cd Stanford/
	../../build/City4CFD config_bpg.json --output_dir results



