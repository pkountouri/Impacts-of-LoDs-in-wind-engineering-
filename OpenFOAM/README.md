# CFD simulations 

OpenFOAM is an open-source computational fluid dynamics (CFD) software package that can 
simulate a range of fluid flow problems. The open-source can be found: 

https://github.com/OpenFOAM


CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Requirements
 * Implementation
 

INTRODUCTION
------------
OpenFOAM is a free and open-source software for computational fluid dynamics simulations.
It provides a wide range of solvers and utilities for modeling and simulating various fluid
flow problems.


REQUIREMENTS
------------
To successfully run simualtions, the following steps are required:

	1. Mesh generation
	2. Define initial conditions
	3. Define boundary conditions
	4. Mesh convergence analysis
	5. Run simulation

There are three main folders needed to start a simulation: 

	* 0 : contains the boundary and initial conditions
	* constant : contains files and subfolders related to the case's constant data (i.e polyMesh, transportProperties, turbulenceProperties)
        * system : is the control folder of the simualtion


IMPLEMENTATION
-------------
After installing the open-source software OpenFOAM on your computer by following the steps mentioned on
the corresponding GitHub page, it is an easy task to run simulations 
by following the next set of commands:

	blockMesh
	surfaceFeautures
	decomposePar
	nohup mpirun -np 32 snappyHexMesh -parallel > log.SHM &
	reconstructParMesh
	rm -r processor*
	cp -r 0/* 2/
	decomposePar
	nohup mpirun -np 32 simpleFoam -parallel > log.SF &
	reconstructPar -latestime



