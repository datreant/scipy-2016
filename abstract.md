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

<!-- Shortly introduce the problem datreant solves -->
In many fields of science one has to store various different kinds of data
,MD-simulation, experimental data and analysis, related to a project. Often the
filesystem serves as a de-facto database for scientific projects, and directory
trees are the zeroth-order data structure for scientific data. But it can be
tedious and error prone to work with these directory trees.

<!-- Introduce datreant -->
To address this problem, we present [**datreant**][datreant]. datreant makes
working with directory structures and files Pythonic by using **Treants**:
specially marked directories with distinguishing characteristics that can be
discovered, queried, and filtered.

<!-- Give a rough overview of what can be done. -->
<!-- This should talk about aggregate and filter methods concretelly. You are
introducing new ords that are specific to datreant (Bundle, View). These should
be explained a little bit otherwise it might leave people confused -->
Named after the walking, talking trees of D&D lore, Treants make it easy to
quickly gather up results from many studies scattered throughout a filesystem,
operate on their stored data based on their characteristics, and store results
again as necessary within their directory trees. datreant also gives Tree and
Leaf classes for granular manipulation of individual directories and files,
respectively, in addition to Bundles and Views for working with many Treants,
Trees, and Leaves as a collective.

<!-- Go into details of implementation -->
[**datreant**][datreant] is a namespace package, with the core components
available from the [datreant.core][datreant.core] module. All the core datreant
objects are extendable; an example of this is [datreant.data][datreant.data],
which provides a convenience interface for storing and retrieving `numpy` and
`pandas` data structures in HDF5 using h5py and PyTables internally.

<!-- Show of general usability of the library with MDSynthesis as example -->
It is also easy to build other applications for data-management on of
[**datreant**][datreant]. We have already build a new library to manage
molecular dynamics data called [MDSynthesis][MDSynthesis].
<!-- Extend this paragraph -->

All current datreant subpackages are openly developed and freely available under
a BSD 3-clause license. More information on how to use the software, as well as
how to get involved, can be found on the [datreant website][datreant].

[datrant]: http://datreant.org/
[datreant.core]: https://github.com/datreant/datreant.core
[datreant.data]: https://github.com/datreant/datreant.data
[MDSynthesis]: https://github.com/datreant/MDSynthesis
