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

Installation
============

Pyqcm is written in Python and thus requires no compilation.
However, it is based on a C++ library (**qcm**) provided with the distribution, and depends on **CUBA** for numerical integration and 
**BLAS-LAPACK** for elementary (non sparse) linear algebra.

The source code can be cloned with the following command::

    git clone https://dsenech@bitbucket.org/dsenechQCM/qcm_wed.git

or, from github::

    git clone https://github.com/dsenech/qcm_wed.git
    git checkout master

Compiling can be done with pip::

    cd <path_to_qcm_wed_folder>
    pip install .



