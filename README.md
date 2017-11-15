# BLPG Solver

Code from https://bitbucket.org/rajgurung777/simplexprojects/downloads/

## Windows Pre-requisites

Download boost source and build

* Go to were the extracted boost files are e.g. c:\boost_1_57_0.
* Run on booststrap.bat This will produce b2, and bjam.
* Run b2 wait.... If you have multiple version of VS then you will need to run from command line and select version e.g. `b2 toolset=msvc-12.0`
* Run bjam and wait... The result will be a folder called stage in the boost file directory.

Extract GLPK for windows

## Environment variables

Create a `BOOST_DIR` system environment variable pointing to the boost files location e.g.

	BOOST_DIR=c:\boost_1_57_0

Create a `GLPK_DIR` system environment variable pointing to the glpk `src` directory (the src directory not the root extraction directory) e.g.

	GLPK_DIR=c:\glpk-4.63\src

## Building

Should build in VS2013 with CUDA 8 with changes made. Importantly the definition of `BOOST_UBLAS_USE_INDEXED_ITERATOR` avoids some problems in the boost ublas header builds.

If you are using boost other than 1.57 or MSCV other than v120 then you will need to modify the library file name for `libboost_timer-vc120-mt-gd-1_57.lib` in the Project->Linker->Input->Additional Dependencies setting.

