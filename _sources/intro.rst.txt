############
Introduction
############

What is pyqcm?
==============

pyqcm is a python module that interfaces with a library written in C++: **qcm**.
This library provide a collection of functions that help implement quantum cluster methods.
Specifically, it provides an exact diagonalization solver for small clusters on which a Hubbard-like model is defined and provides functions to define infinite-lattice models and to embed the clusters into the lattice via *Cluster Pertrubation Theory* (CPT). Methods like the *Variational Cluster Approximation* (VCA) and *Cluster Dynamical Mean Field Theory* (CDMFT) are then implemented from qcm by the pyqcm module, which is written in Python only.

This document is not a review of the above methods; the reader is referred to the appropriate review articles for that. It is strictly a user's manual for the pyqcm module.
Some degree of understanding of the above methods is however necessary to proceed.
This document also provides insights as to the inner working of the code, and therefore consitutes also a embryonic developer's manual.

Requirements
============

Pyqcm is written in Python and thus requires no compilation.
However, the following librairies are needed:

**qcm**. The source code can be cloned with the following command::

    git clone https://dsenech@bitbucket.org/dsenech/qcm_wed.git

It is written in C++, and requires lapack and python3 for interfacing. It also contains the pyqcm python module.

**CUBA** (http://www.feynarts.de/cuba/) is required by qcm for performing integrals in dimension > 2 (hence the name, for *cubature*). qcm uses version 4.0 or above. Version 2.1 is not supported. However, the CUBA library must be compiled with a modified makefile in order to use it within another shared library (the option -fPIC must be added. See the file `INSTALL` included in the distribution for details).

**BLAS-LAPACK**. Needed for efficient vector and matrix operations.

Compiling qcm
========================

Please consult the INSTALL files in each library's distribution to see how to compile and install the libraries.
The shared object file qcm.so should be somewhere in the system's Python path.

