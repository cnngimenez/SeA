
# Table of Contents

1.  [SeA](#org284f875)
2.  [Libraries and packages](#orgc498390)
3.  [Compiling](#org2b8f872)
    1.  [With GPRBuild](#orgeca7a91)
4.  [Usage](#orgb9e0bad)
5.  [License](#orgcd79205)


<a id="org284f875"></a>

# SeA

SeA are Ada libraries for the Semantic Web

![img](https://img.shields.io/badge/License-GPLv3-informational.png?logo=gnu) ![img](https://img.shields.io/badge/Ada-2012-informational.png)


<a id="orgc498390"></a>

# Libraries and packages

![img](imgs/libraries.png)
See imgs/README.md for the Semantic Web stack image copyright.

SeA are divided in the following packages:

![img](imgs/packages.png)


<a id="org2b8f872"></a>

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


<a id="orgeca7a91"></a>

## With GPRBuild

Use the following commands to compile:

    gprbuild -PSeA.gpr -p

To install the library and binaries:

    gprinstall -PSeA.gpr -p

A install directory can be specified by the `--prefix` parameter:

    gprinstall -PSeA.gpr --prefix=/home/USERNAME/Ada -p


<a id="orgb9e0bad"></a>

# Usage

The API specification are available as `*.ads` files. 

Librares can be used by importing the GPR file into your GPR. For instance, the SeA-turtle imports the SeA-common libraries on their `turtle_lib.gpr` with the following sentence:

Main programs were created for debuging purposes. They usually are `src/binaries/*.adb` source files and they are specified inside the `PROJECTNAME_binaries.gpr` file at the `Main` variable.
These programs are used to test and debug the libraries. They can be used as examples.


<a id="orgcd79205"></a>

# License

This work is under the General Public License version 3.

