Abstract for SciPy 2016 (Talk)
==============================

Title
-----
datreant: persistent, Pythonic trees for heterogeneous data

Authors
-------
- David L. Dotson     (david.dotson@asu.edu)
- Sean L. Seyler      (sean.seyler@asu.edu)
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
simulation data, there is often an existing ecosystem of specialized tools and
file formats which new tools must work around, for better or worse.
Furthermore, centralized database solutions may be suboptimal for data storage
for a number of reasons, including insufficient hardware infrastructure,
variety and heterogeneity of raw data, the need for data portability, etc.
This is particularly the case for fields centered around simulation: simulation
systems can vary widely in size, composition, rules, paramaters, and starting
conditions. And with increases in computational power, it is often necessary to
store intermediate results obtained from large amounts of simulation data so it
can be accessed and explored interactively.

The result of this state of affairs is that the filesystem often serves as a
de-facto database for scientific projects, and directory trees the zeroth-order
data structure for scientific data. But it can be tedious and error prone to
work with these directory trees directly from the shell or from Python scripts
that operate on hard-coded paths. There is almost certainly a better way.

To address this problem, we present **datreant**. datreant makes working with
directory structures and files Pythonic, and in particular it introduces
**Treants**: specially marked directories with distinguishing characteristics
that can be discovered, queried, and filtered. 

Named after the walking, talking trees of D&D lore, Treants make it easy to
quickly gather up results from many studies scattered throughout a filesystem,
operate on their stored data based on their characteristics, and store results
again as necessary within their directory trees. datreant also gives Tree and
Leaf classes for granular manipulation of individual directories and files,
respectively, in addition to Bundles and Views for working with many Treants,
Trees, and Leaves as a collective.

**datreant** is a namespace package, with the core components available from
the [datreant.core](https://github.com/datreant/datreant.core) module. All
the core datreant objects are extendable with specialized limbs supplied by
other datreant subpackages; an example of this is
[datreant.data](https://github.com/datreant/datreant.data), which provides a
convenience interface for storing and retrieving `numpy` and `pandas` data
structures in HDF5 using h5py and PyTables internally.

All current datreant subpackages are openly developed and freely available
under a BSD 3-clause license. More information on how to use the software,
as well as how to get involved, can be found on the datreant website:
http://datreant.org/
