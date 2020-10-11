
# Table of Contents

1.  [SeA](#org599f359)
2.  [Libraries and packages](#orge703731)
3.  [Compiling](#org5d9932f)
    1.  [With GPRBuild](#orgf412815)
4.  [Usage](#orgd0b7fd9)
5.  [License](#org42cdc92)


<a id="org599f359"></a>

# SeA

SeA are Ada libraries for the Semantic Web

![img](https://img.shields.io/badge/License-GPLv3-informational.png?logo=gnu) ![img](https://img.shields.io/badge/Ada-2012-informational.png)


<a id="orge703731"></a>

# Libraries and packages

-   [SeA\_common](https://github.com/cnngimenez/SeA-common)
-   [SeA\_turtle](https://github.com/cnngimenez/SeA-turtle)
-   [Sea\_redstore](https://github.com/cnngimenez/SeA-redstore)

![img](imgs/libraries.png)
See imgs/README.md for the Semantic Web stack image copyright.

SeA are divided in the following packages:

![img](imgs/packages.png)


<a id="org5d9932f"></a>

# Compiling

All SeA subpackage follows the usual procedure.

The requirements are

-   the Ada GNAT compiler
-   the GPRBuild tools
-   the [Matreshka library](https://forge.ada-ru.org/matreshka)
-   the [ada-utils library](https://github.com/stcarrez/ada-util/)

The usual sequence may work for your environment:

    make
    make install

The Makefile can be configure at the makefile.setup file. This file can be generated with the following command:

    make setup


<a id="orgf412815"></a>

## With GPRBuild

Use the following commands to compile:

    gprbuild -PSeA.gpr -p

To install the library and binaries:

    gprinstall -PSeA.gpr -p

A install directory can be specified by the `--prefix` parameter:

    gprinstall -PSeA.gpr --prefix=/home/USERNAME/Ada -p


<a id="orgd0b7fd9"></a>

# Usage

The API specification are available as `*.ads` files. 

Librares can be used by importing the GPR file into your GPR. For instance, the SeA-turtle imports the SeA-common libraries on their `turtle_lib.gpr` with the following sentence:

Main programs were created for debuging purposes. They usually are `src/binaries/*.adb` source files and they are specified inside the `PROJECTNAME_binaries.gpr` file at the `Main` variable.
These programs are used to test and debug the libraries. They can be used as examples.


<a id="org42cdc92"></a>

# License

This work is under the General Public License version 3.

