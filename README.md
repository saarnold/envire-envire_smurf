Envire SMURF
=============
Provides the tools to load populate a envire representation from a SMURF or URDF model.

The model of the robot that is stored either as URDF or as SMURF (extension of URDF) can be uploaded to a Envire TransformationGraph with this tool. The components of the robot are localized as nodes, the edges of the graph store the relative positions (transformations) between the nodes they connect.

The tool also allows to load other objects (not only robots) defined in the SMURF file.

License
-------
GPL-v2 or later

Installation
------------
The easiest way to build and install this package is to use Rock's build system.
See [this page](http://rock-robotics.org/stable/documentation/installation.html)
on how to install Rock.

However, if you feel that it's too heavy for your needs, Rock aims at having
most of its "library" packages (such as this one) to follow best practices. See
[this page](http://rock-robotics.org/stable/documentation/packages/outside_of_rock.html)
for installation instructions outside of Rock.

Rock CMake Macros
-----------------

This package uses a set of CMake helper shipped as the Rock CMake macros.
Documentations is available on [this page](http://rock-robotics.org/stable/documentation/packages/cmake_macros.html).

Rock Standard Layout
--------------------

This directory structure follows some simple rules, to allow for generic build
processes and simplify reuse of this project. Following these rules ensures that
the Rock CMake macros automatically handle the project's build process and
install setup properly.

STRUCTURE
-- src/ 
	Contains all header (*.h/*.hpp) and source files
-- build/
	The target directory for the build process, temporary content
-- bindings/
	Language bindings for this package, e.g. put into subfolders such as
   |-- ruby/ 
        Ruby language bindings
-- viz/
        Source files for a vizkit plugin / widget related to this library 
-- resources/
	General resources such as images that are needed by the program
-- configuration/
	Configuration files for running the program
-- external/
	When including software that needs a non standard installation process, or one that can be
	easily embedded include the external software directly here
-- doc/
	should contain the existing doxygen file: doxygen.conf
