About example-package
=====================

* Home: http://example.com
* Package license: BSD-3
* Feedstock license: BSD
* Summary: An example package which does not contain anything


Installing example-package
==========================

Installing example-package from the janschulz channel can be achieved by adding
"janschulz" to your channels with:

```
conda config --add channels janschulz
```

Once the "janschulz" channel has been enabled, example-package can be installed with:

```
conda install example-package
```

It is possible to list all of the versions of example-package available on your platform with:

```
conda search example-package --channel janschulz
```



Terminology
===========

**feedstock** - a repository with one or more conda recipes (raw material), supporting scripts and
                CI configuration

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - a github organisation which builds `conda smithy` and produces conda packages
                  for the `conda-forge` channel.

Current build status
====================
Linux: [![Circle CI](https://circleci.com/gh/JanSchulz/example-package-feedstock.svg?style=svg)](https://circleci.com/gh/JanSchulz/example-package-feedstock)
OSX: [![TravisCI](https://travis-ci.org/JanSchulz/example-package-feedstock.svg?branch=master)](https://travis-ci.org/JanSchulz/example-package-feedstock)
Windows: [![AppVeyor](https://ci.appveyor.com/api/projects/status/github/JanSchulz/example-package-feedstock?svg=True)](https://ci.appveyor.com/project/JanSchulz/example-package-feedstock/branch/master)


Updating example-package-feedstock
==================================

If you would like to improve the example-package recipe, please take the normal
route of forking this repository and submitting a PR. Upon submission, your changes will
be run on the appropriate platforms to give the reviewer an opportunity to confirm that the
changes result in a successful build. Once merged, the recipe will be re-built and uploaded
automatically to the "janschulz" channel, whereupon they will be available for everybody to
install and use.



In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of one or more conda recipes (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge) or your own channel at the
[Anaconda-Cloud](http://docs.anaconda.org/) for Linux, Windows and OSX
respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to regenerate all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy regenerate``.