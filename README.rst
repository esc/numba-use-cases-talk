====================
Numba Use-Cases Talk
====================

Numba use-cases talk.

Summary
=======

Numba is a Python just-in-time (JIT) compiler that has a significant number of
dependent projects.  That is: software packages beyond the prototype
stage that depend directly on Numba. In this talk I will discuss what specific
use-cases Numba solves, how it is being used in dependents and what the
leveraged benefits are -- including some insightful statistics. I will also
show-case multiple personal favorites of this ecosystem and highlight the merit
and value they bring to the broader open source community. I will conclude with
some thoughts on challenges and opportunities that come with maintaining a
low-level library with such an impact, i.e. a significant number of dependent
projects.


Abstract
========

In this talk I will begin with a short introduction to Numba, a just-in-time,
type-specializing, function compiler for accelerating numerically-focused
Python. Then I will focus on how to actually count it's dependent projects,
what systems can be queried to determine this figure, how accurate it might be
and how we may aggregate across systems to summarize this. For example, Github
lists over 150k repositories and over 6k packages as direct dependents of
Numba, but this probably includes personal projects and forks and so this
number is likely to be rather inflated. Conda-forge on the other hand lists 139
total dependent projects, which is probably a much more realistic number of
mature, nontrivial dependents.

Then, I will continue with an overview of the most important use-case of Numba
and highlight some personal favorites as examples. First, acceleration of pure
Python code that can not be expressed as operations on NumPy arrays or
accelerating code written as NumPy operations -- for example librosa and UMAP.
Second, Compiling user-defined functions for use in existing packages and
algorithms for example -- Pandas, VectorDB and also the Caterva2 compressed
compute engine. Third, shipping fast packages that do not need compiled
c-extensions and thus eliminating use of C/C++ to accelerate a project -- for
example Tardis-SN. Fourth, using Numba to compile Python code to run on GPUs
and other hardware targets -- for example PyOMP, numba-cuda (for NVIDIA GPUs)
and numba-hip (for AMD-GPUs). Fifth, accelerating database query and access
routines -- for example NumbaDuck, the fully JITted interface to the popular
DuckDB, and NumbSQL, a Numba based interface to SQLite.

Lastly, I will discuss the challenges and opportunities that come with
maintaining a popular low-level library. Such as the need for rigorous
testing and a solid release process that makes use of release candidates.

Licensing
=========

Content
-------

All Content is...

* Copyright 2025 Valentin Haenel <valentin@haenel.co>
* Licensed under the terms of `Attribution-ShareAlike 3.0 Unported  (CC BY-SA 3.0)  <http://creativecommons.org/licenses/by-sa/3.0/>`_
