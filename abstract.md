Abstract for SciPy 2016 (Talk)
==============================

Title
-----
datreant: persistent, Pythonic trees for heterogeneous data

Authors
-------
- David L. Dotson     (david.dotson@asu.edu)
- Sean L. Seyler      (sean.seyler@asu.edu)
- Max Linke           (max.linke@biophys.mpg.de)
- Richard Gowers      (richardjgowers@gmail.com)
- Oliver Beckstein    (oliver.beckstein@asu.edu)

Target track
------------
Must choose one:
- Scientific Computing in Python (General track)
- Python in Data Science

Abstract (approx. 100 words)
----------------------------
> The brief description you fill out below will appear in the online program.


Long Description (approx. 200-500 words)
----------------------------------------
> Your placement in the program will be based on reviews of your detailed
> description. This should be a 200-500 word detailed outline of your
> presentation. This outline should concisely describe software of interest to
> the SciPy community, tools or techniques for more effective computing, or how
> scientific Python was applied to solve a research problem. A traditional
> background/motivation, methods, results, and conclusion structure is
> encouraged but not required. Links to project websites, source code
> repositories, figures, full papers, and evidence of public speaking ability
> are encouraged.

In many fields of science, especially those analyzing experimental or
simulation data, there is an existing ecosystem of specialized tools and file
formats which new tools must work around. Often this makes the filesystem serve
as a de-facto database, with directory trees the zeroth-order data structure
for scientific data. But it can be tedious and error prone to work with these
directory trees to retrieve and store datasets.

To address this problem, we present [**datreant**](http://datreant.org/).
datreant makes working with directory structures and files Pythonic with
**Treants**: specially marked directories with distinguishing characteristics
that can be discovered, queried, and filtered.

Treants make it easy to quickly gather up results from many studies scattered
throughout a filesystem, operate on their stored data based on their
characteristics, and store results again as necessary within their directory
trees. datreant also gives Tree and Leaf classes for granular manipulation of
individual directories and files, respectively, in addition to Bundles and
Views for working with many Treants, Trees, and Leaves as a collective.

[**datreant**](http://datreant.org) is a namespace package, with the core
components available from the
[datreant.core](https://github.com/datreant/datreant.core) module. All core
datreant objects are extendable; an example of this is
[datreant.data](https://github.com/datreant/datreant.data), which provides a
convenience interface for storing and retrieving `numpy` and `pandas` data
structures in HDF5 using h5py and PyTables internally.

**datreant** is also designed with specialized applications for data management
in mind. [**MDSynthesis**](https://github.com/datreant/MDSynthesis) is built on
top of datreant, and makes working with molecular dynamics (MD) simulation data
easier with **Sim** objects. These are **Treants** that use
[MDAnalysis](http://www.mdanalysis.org/) to dissect MD trajectories, with
mechanisms for storing system definitions and custom atom selections. These
make it possible to write maintainable analysis code that works across many
simulation variants.

All current datreant subpackages are openly developed and freely available
under a BSD 3-clause license. More information on how to use the software,
as well as how to get involved, can be found on the [datreant
website](http://datreant.org/).
