MPHY0022CW1
------------------

[![Build Status](https://travis-ci.com/MattClarkson/MPHY0022CW1.svg?branch=master)](https://travis-ci.com/MattClarkson/MPHY0022CW1)
[![Build Status](https://ci.appveyor.com/api/projects/status/5pm89ej732c1ekf0/branch/master)](https://ci.appveyor.com/project/MattClarkson/cmakecatch2)


Purpose
-------

This is the first coursework for UCL's Research software computing with C++ MPHYG0022 module. It only includes
Normal equation and QR decomposition methods for solving least squared linear regression. The data dealing with is a
pair of x(observed) and y(prediction) values. This is a simple Least square regression. For example, the x values can
be house sizes and the y values can be the house prices.
For more information about the Linear regression see hands on machine learning with scikit-learn and tensorflow
(Aurelion Gèron) or Machine learning and pattern recognition(Christopher Bishop).

The Template for the CMake was cloned from https://github.com/MattClarkson/MPHY0022CW1.git.

Credits
-------

This project was developed as a teaching aid for UCL's ["Research Computing with C++"](http://rits.github-pages.ucl.ac.uk/research-computing-with-cpp/)
course developed by [Dr. James Hetherington](http://www.ucl.ac.uk/research-it-services/people/james)
and [Dr. Matt Clarkson](https://iris.ucl.ac.uk/iris/browse/profile?upi=MJCLA42).
The code was modified for the purpose of this assignment by D.W.

The Template for the CMake was cloned from https://github.com/MattClarkson/MPHY0022CW1.git.

Contents of the Repository
--------------------------
All the header files are in Code/Lib.
The source files added to existing directory are:
mphyBasicTypes.cpp
mphyException.cpp
ConcreteGetData.cpp
ConcreteFitData.cpp
ConcreteQR.cpp
Reader.cpp
  ../CommandLineApps/main.cpp

The header files added to existing directory are:
GetData.h
ConcreteGetData.h
FitData.h
ConcreteFitData.h
Reader.h

In the Testing Directory I have my all my Unit tests in the file:
ConcreteGetDataTests.cpp (legacy of following the assignments instructions from the begininng).


Short Build Instructions
------------------
You need to have CMake installed to install this project. For instructions on installing CMake see next sections.
This project uses CMake to build the tree.

A very short way of using it for Linux terms is as follows:
would be:
``` cmake
git clone $github repository (no repository yet)$
mkdir MPHY0022CW1-Build
cd MPHY0022CW1-Build
cmake ../MPHY0022CW1
make
```

3rd Party packages
------------------
This project requires the packages Eigen and optionally Boost.
Your compiler would find the Eigen file, since it is a a header-only file and is included in the repository. However,
if it can't find it copy the folder into the location specified by your compiler.


Running the Command Line
-----------------------
You can use a command line app to run the program from the terminal. The command line app is named main and is stored in
bin folder of the build directory. To evoke the app do:
'''
./bin/main
'''
This will give you the help command which would otherwise be evoked with the -h or -help argument.

This command line needs to arguments. First argument is the name of the solver, choose from "Normal" (Normal equation)
or "QR" (QR decomposition method). The second argument is the text file containing the x and y values.The text file of
data should have the value of x and y in each line. Otherwise there would be an exception thrown.

Installing Cmake for OSX, UNIX, LINUX
--------------------
You can download pre-compiled binaries from http://cmake.org/download/ . You can also build CMake from source. If no
pre-existing CMake installation exists, use a bootstrap script:
'''
./bootstrap
  make
  make install
  '''
For more information about bootstrap run ./bootstrap --help .

In case an Exisitng CMake installation exist, run the following to build a newer version:
'''
  cmake .
  make
  make install
'''

Installing Cmake for Windows
--------------------
Download  a pre-compiled library from http://cmake.org/download/ page for windows as a zip file. You could also download
and build CMake from source. To build the CMake from a source tree on Windows, first install the latest binary version
of CMake. Then, run it on CMake as you would run any other project. This means selecting CMake as the Source Directory
and then selecting a binary directory for the resulting executables



