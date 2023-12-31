# QNMorpho
Quantifying Neuronal Branched Morphologies 

This package is developed by Sabyasachi Sutradhar. This MATLAB-based package can be used to quantify many properties of branched neuronal structures. Some of the properties are listed below:
1.	Location of the Soma
2.	Size of the neuron (Convex Hull diameter, Area, etc.)
3.	Skeletonized neuron structure
4.	Neuronal Radius of gyration
5.	Number and lengths of branches and tips
6.	Branch and branchpoint locations (xy coordinates)
7.	Branch persistence length
8.	Fractal Dimension and Mesh size of neuron
9.	Branch ordering and connection map.

Copyright: Sabyasachi Sutradhar (Sabyasachi.sutradhar@yale.edu), 2022

License:

Creative Commons Legal Code

Installation: This package plugin for MATLAB. Just download it and double-click. It will be added to your MATLAB apps.


Algorithm
To quantify the characteristics of branched neuronal structures, the following steps are employed:

1.	Binarization and Skeletonization of Images: The input images are first converted into binary representations and subsequently skeletonized.
2.	Soma Localization: To identify the location of the soma, thin branches are eroded, and the soma's centroid is determined.
3.	Alignment: A breadth-first search algorithm is employed to align the skeletonized points of the soma with the overall structure of branched neurons.
4.	Branch Smoothing: Individual branches are smoothed using a spline fitting technique to obtain coordinated, smooth branch outlines.
5.	Branchpoint and Endpoint Detection: MATLAB's 'bwmorph' function is utilized to detect branchpoints and endpoints.
6.	Small-Scale Properties: Small-scale properties like the fractal dimension are computed using the box-counting method.
7.	Mesh Size Calculation: The mesh size is determined based on the method outlined in Ganguly et al. (2016) arXiv.
8.	Topological Calculations: Two key metrics are employed for topological analysis. First, the calculation of leaf nodes follows the approach introduced by Liao et al.2020,PNAS. Subtree size calculation adheres to the method presented by Hannezo et al, 201, Cell. Additionally, the software computes the Strahler number of the branches.



Limitations
It's essential to be aware of the limitations of this package:

Signal-to-Noise Ratio Requirement: This package performs optimally when provided with high-quality images with a good signal-to-noise ratio. It may struggle to establish branch connections in the presence of looped structures within the branches.

Looped Structure Handling: In cases where looped structures exist in the neuronal branches, manual image editing may be required to eliminate these loops before applying the algorithm.

Image Type: This software is specifically designed to process grayscale images (8/16 bit). Ensure that your images are in the appropriate format for accurate analysis. 

Here is a look of the software:

![Screenshot 2023-10-16 at 2 19 40 PM (2)](https://github.com/SabyasachiSutradhar/QNMorpho/assets/49563656/587f6e2a-e2e2-477d-a344-9e4b8441ba07)

Acknowledgment:
Sonal Shree for providing the experimental images.



