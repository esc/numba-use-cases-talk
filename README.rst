====================
Numba Use-Cases Talk
====================

Numba use-cases talk.

Summary
=======

The Python just-in-time (JIT) compiler Numba has a significant number of
non-trivial dependents. That is: software packages beyond the prototype stage
that depend directly on Numba. In this talk I will discuss what specific
use-cases Numba solves, how it is being used in dependents and what the
leveraged benefits are -- including some insightful statistics. I will also
show-case multiple personal favorites of this ecosystem and highlight the merit
and value they bring to the broader open source community. I will conclude with
some thoughts on challenges and opportunities that come with maintaining a
low-level library of this magnitude.


Abstract
========

In this talk I will begin with a short introduction to Numba, the just-in-time,
type-specializing, function compiler for accelerating numerically-focused
Python. Then I will focus on how to actually count dependents, what approaches
can be used to determine this figure, how accurate it might be and how we may
aggregate across systems to summarize this. So, for example Github lists over
150k repositories and over 6k packages as direct dependents of Numba, but this
probably includes personal projects and forks and so this number is likely to
be rather inflated. Conda-forge on the other hand lists 139 total children,
which is probably a much more realistic number of mature, nontrivial
dependencies.  Following up, I will present some statistical analysis of the
overall Numba ecosystem and present some insightful visualizations of these
statistics.

Then, I will continue with an overview of the most important use-case of Numba
an highlight some personal favorites as examples. Raw acceleration of Python
code, for example as used in Clifford, librosa and UMAP.  Accelerating
user-defined functions for use in existing packages such as Pandas, VectorDB
and also the Caterva2 compressed compute engine. And even accelerating database
query and access routines in the case of NumbaDuck, the fully JITted interface
to the popular DuckDB and also NumbSQL a Numba based interface to SQLite.

Lastly, I will discuss the challenges and opportunities that come with
maintaining a heavily used low-level library.

