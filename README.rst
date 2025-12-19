====================
Numba Use-Cases Talk
====================

What does Numba enable? A maintainer’s journey to discover where and how a
library is being used.

Summary
=======

Numba is a Python just-in-time (JIT) compiler that has a significant number of
dependent projects (dependents).  That is: software packages beyond the
prototype stage that depend directly on Numba. In this talk I will discuss what
specific use-cases Numba solves, how it is being used in dependents and what
the leveraged benefits are -- including some insightful statistics. I will also
show-case multiple personal favorites of this ecosystem and highlight the merit
and value they bring to the broader open source community. I will conclude with
some thoughts on challenges and opportunities that come with maintaining a
popular and  widely used low-level library.


Abstract
========

In this talk I will begin with a short introduction to Numba, a just-in-time,
type-specializing, function orientated compiler for accelerating
numerically-focused Python. Then I will focus on how to actually count its
dependents, what systems can be queried to determine this figure, how accurate
it might be and how we can summarize by aggregating across systems. For
example, Github lists over 150k repositories and over 6k packages as direct
dependents of Numba, but this probably includes personal projects and forks and
so this number is likely to be rather inflated. Conda-forge on the other hand
lists 139 total dependents, which is probably a much more realistic number of
mature, nontrivial dependents.

I will continue with an overview of the most important use-case of Numba and
highlight some personal favorites as examples. First, acceleration of pure
Python code that cannot be expressed as operations on NumPy arrays and the
acceleration of code written as NumPy operations -- for example librosa and
UMAP.  Second, compiling user-defined functions for use in existing packages
and algorithms, for example -- Pandas, VectorDB and also the Caterva2
compressed compute engine. Third, converting an entire code-base from C to
Python in order to significantly reduce the maintenance burden and accelerate
development -- for example Tardis-SN. Fourth, using Numba to compile Python
code to run on GPUs and other hardware targets -- for example PyOMP (OpenMP in
Python), numba-cuda (for NVIDIA GPUs) and numba-hip (for AMD GPUs). Finally,
accelerating database query and access routines -- for example NumbaDuck, the
fully JITted interface to the popular DuckDB, and NumbSQL, a Numba based
interface to SQLite.

To conclude, I will discuss the challenges and opportunities that come with
maintaining a popular low-level library. Such as the need for rigorous testing,
declared support tiers, and a well defined and communicated release process.

Licensing
=========

Content
-------

All Content is...

* Copyright 2025 Valentin Haenel <valentin@haenel.co>
* Licensed under the terms of `Attribution-ShareAlike 3.0 Unported  (CC BY-SA 3.0)  <http://creativecommons.org/licenses/by-sa/3.0/>`_
