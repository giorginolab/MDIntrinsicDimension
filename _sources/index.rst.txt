.. IntrinsicDimension documentation master file, created by
   sphinx-quickstart on Tue Jul 22 21:26:48 2025.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

MDIntrinsicDimension - Intrinsic dimension estimation along molecular dynamics simulations
==========================================================================================


Many biological datasets, such as those derived from molecular dynamics (MD) simulations, are described by high-dimensional feature vectors. 
However, lot of these features are redundant, often due to correlations in the data. 
In such cases, the actual dynamics of the system can be projected onto a lower-dimensional manifold without significant loss of information. 

The therm *Intrinsic Dimension* (ID) intuitively refers to the minimum number of variables needed to describe the essential structure of such a dataset.
Under the manifold hypothesis, which assumes that high-dimensional data lie on a lower-dimensional manifold, ID estimation aims to determine the minimum dimensionality of said manifold. 

This package is specifically designed to address the ID estimation of proteins molecular dynamics simulations.

Workflow
^^^^^^^^^^^^^^^^^^^^^^^^
Provided a MD trajectory, the **MDIntrinsicDimension** package performs two things:

1. Computes the projection
2. Estimates ID

Projections are included in the ID estimation procedure as the initial step of dimensionality reduction to remove non-interesting movements such as global rigid-body translations and rotations.
After this initial step, ID is computed.


Functionalities
^^^^^^^^^^^^^^^^^^^^

It includes three functions and as many analysis modes:    

- `intrinsic_dimension`: ID on whole molecule. 
- `section_id`: ID on fixed sliding window along protein's sequence.    
- `secondary_structure_id`: ID on contiguous secondary structure elements.  
 
.. toctree::
   :maxdepth: 1
   :caption: TUTORIAL
   
   installation
   quickstart
   villin_data.ipynb
.. toctree::
   :maxdepth: 1 
   :caption: EXAMPLES
   :hidden:
   


   villin_plots.ipynb
   NTL9_plots.ipynb
   estimators.ipynb
   projections.ipynb
   rmsd.ipynb

   

 
 
