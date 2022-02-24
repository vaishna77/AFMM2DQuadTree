This code needs Eigen libary. Download the latest stable version from https://eigen.tuxfamily.org/index.php?title=Main_Page

This is a 2D FMM Code to perform Matrix-Vector products of the form Ax.

It is a completely algebraic version. Compressions are made via ACA.

It is applicable to all FMM-able and symmetric kernels.

Follows the usual FMM quad tree data structure.

The kernel that defines the matrix A is to be defined in "kernel.hpp" file.

The vector x is to be defined in  "kernel.hpp" file.

"ACA.hpp" file contains the ACA module.

"FMM2DTree.hpp" file contains the algorithm.

Before running make sure Eigen and openmp library paths are specified in Makefile.

It takes these inputs at run time: number of Levels in tree, Number of particles in leaf along 1D, Half side length of the square domain, tol of ACA in negative powers of 10

To run it input in terminal:

make -f Makefile2D.mk clean

make -f Makefile2D.mk

./testFMM2D 6 5 1 8

The output looks like:

Number of particles is: 102400

Time taken to create the tree is: 0.005085

Time taken to assemble is: 11.6754

Time taken to do Mat-Vec product is: 0.359461

Performing error calculation in box: 1002

err: 1.8609e-07
