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

In science the filesystem often serves as a *de facto* database, with directory
trees being the zeroth-order scientific data structure. But it can be tedious
and error prone to work directly with the filesystem to retrieve and store
heterogeneous datasets. **datreant** makes working with directory structures
and files Pythonic with **Treants**: specially marked directories with
distinguishing characteristics that can be discovered, queried, and filtered.
Treants can be manipulated individually and in aggregate, with mechanisms for
granular access to the directories and files in their trees. Disparate datasets
stored in any format (CSV, HDF5, NetCDF, Feater, etc.) scattered throughout a
filesystem can thus be manipulated as meta-datasets of Treants. **datreant**
is modular and extensible by design to allow specialized applications to be
built on top of it, with **MDSynthesis** as an example for working with
molecular dynamics simulation data.  http://datreant.org/


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
as a *de facto* database, with directory trees the zeroth-order data structure
for scientific data. But it can be tedious and error prone to work with these
directory trees to retrieve and store heterogeneous datasets, especially over
projects spanning years with no strict organizational scheme.

To address this pain point, we present [**datreant**](http://datreant.org/).
At the core of datreant are **Treants**: specially marked directories with
distinguishing characteristics that can be discovered, queried, and filtered.
Treants map the filesystem as it is into a Pythonic interface, making
heterogeneous data easier to leverage while enhancing scientific
reproducibility.

Treants make it easy to quickly gather datasets stored within many files in any
format (CSV, HDF5, NetCDF, Feather, etc.) scattered throughout a filesystem,
operate on these data, and store results again as necessary within the Treants'
directory trees. **datreant** also provides Tree and Leaf classes for granular
manipulation of individual directories and files, respectively, as well as
Bundles and Views for working with aggregations of many Treants, Trees, and
Leaves. Bundles in particular can filter Treants based on tags, and perform
group-by operations on their categories. In this way, disparate datasets can be
powerfully manipulated as meta-datasets of Treants. And because Treants are  
filesystem objects, they can be used alongside other tools, such as
[dask.distributed](http://distributed.readthedocs.org/), to distill knowledge
from data more effectively.

[**datreant**](http://datreant.org) is a namespace package, with the core
components available in the dependency-light
[datreant.core](https://github.com/datreant/datreant.core) module. All core
datreant objects are extendable; an example of this is
[datreant.data](https://github.com/datreant/datreant.data), which provides a
convenience interface for storing and retrieving `numpy` and `pandas` data
structures in HDF5 using h5py and PyTables internally.

**datreant** is also designed with specialized applications for data management
in mind. For working with molecular dynamics (MD) simulation data,
[**MDSynthesis**](https://github.com/datreant/MDSynthesis)--built on top of
datreant--streamlines workflow through **Sim** objects. **Sims** are special
**Treants** that use [MDAnalysis](http://www.mdanalysis.org/) to dissect MD
trajectories, providing mechanisms for storing system definitions and custom
atom selections. This makes it possible to write maintainable analysis code
that works across many simulation variants. Just as importantly, Sims allow
rapid interactive work drawing from hundreds of simulations at once, making
scientific questions easier to answer with less time and effort.

All current datreant subpackages are openly developed and freely available
under a BSD 3-clause license. More information on how to use the software,
and how to get involved, can be found at http://datreant.org/
