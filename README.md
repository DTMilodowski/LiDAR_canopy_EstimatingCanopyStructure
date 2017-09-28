# LiDAR_canopy
**David T. Milodowski**, School of GeoSciences, University of Edinburgh

(September 2017)
----------------

This repository hosts a python library to extract quantitative information about forest canopies from discrete return LiDAR point clouds. It includes all the driver functions required to reproduce the analysis presented in the manuscript: "Estimating Canopy Structure Across A Degradation Gradient In Malaysian Borneo", submitted to Remote Sensing Of Environment.

## What is in the repository?
This repository hosts code currently under development.  Not all the functions listed in the modules are used in the analysis, as there are some relict functions from previous iterations, and some functions that are currently being used in other projects. The scripts *highlighted* are driver functions used to undertake the analysis presented in the manuscript - that is they call the relavent subroutines from the other modules.

- LiDAR_io.py : Interfacing with laspy for i/o and spatial filtering of LiDAR returns based on neighbourhood or polygon boundaries; also constructs kdtrees
- LiDAR_tools.py : a bunch of useful tools to interact with LiDAR in python includes spatial filtering of LiDAR returns based on neighbourhood or polygon boundaries.
- auxilliary_functions.py : some generic useful stuff
- LiDAR_MacHorn_LAD_profiles.py : this code calculates the vertical leaf area distribution (_sensu stricto_ plant area distribution) using the method proposed by Stark et al. [Ecology Letters, 2012], which utilises the MacArthur-Horn-based approach to invert the vertical distribution of first returns
- LiDAR_radiative_transfer_LAD_profiles.py : this code calculates the vertical leaf area distribution (_sensu stricto_ plant area distribution) using the method proposed by Detto et al. [Journal of Geophysical Research, 2015], which inverts LiDAR distributions based on a stochastic radiative transfer model.  This includes modifications to the model by me to account for variable absorption of LiDAR pulses by canopy material.
- inventory_based_LAD_profiles.py : some code to produce crown volume distribution estimates based on detailed field observations and/or allometric relationships
- least_squares_fitting.py : routines to perform least squares fitting of various types, including polynomial and surface fitting, and affine transformations
- create_subplot_grids_least_squares_affine_transformation.py : a driver function to fit subplot grids to GEM plot vertices using a least squares affine (rotation & translation) transformation.

- *canopy_structure_paper_figs.py* : driver function to undertake all analysis in manuscript, except for sensitivity analysis
- *structural_sensitivity_analysis.py* : driver function to undertake the sensitivity analysis performed in the manuscript and produce relevant figures

## Contact
If you have any questions regarding the code, please don't hesitate to email me at: d.t.milodowski@ed.ac.uk