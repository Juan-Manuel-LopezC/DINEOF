# DINEOF

[![Build Status Linux](https://travis-ci.org/aida-alvera/DINEOF.svg?branch=master)](https://travis-ci.org/aida-alvera/DINEOF)

DINEOF is an EOF-based method to fill in missing data from geophysical fields, such as clouds in sea surface temperature.

For more information on how DINEOF works, please refer to [Alvera-Azcarate et al (2005)](http://hdl.handle.net/2268/4296) and [Beckers and Rixen (2003)](http://hdl.handle.net/2268/4291). The multivariate application of DINEOF is explained in [Alvera-Azcarate et al (2007)](http://hdl.handle.net/2268/9485), and in [Beckers et al (2006)](http://www.ocean-sci.net/2/183/2006/os-2-183-2006.pdf) the error calculation using an optimal interpolation approach is explained. If you need a copy of any of these papers, don't hesitate to contact us! For more information about the Lanczos solver, see [Toumazou and Cretaux (2001)](https://doi.org/10.1175/1520-0493(2001)129%3C1243:UALEIT%3E2.0.CO;2).


# Help pages
Help pages on how to install and compile DINEOF can be found [here](http://modb.oce.ulg.ac.be/DINEOF).

[FAQ](./docs/FAQ.md)


# Installation

## Linux

### Installation from source
Please follow instruction on the [help pages](http://modb.oce.ulg.ac.be/DINEOF), taking into account that you need to install gfortran, make, Arpack and NetCDF as follows (for Ubuntu and Debian):

```bash
sudo apt-get update
sudo apt-get install gfortran make libarpack2-dev libnetcdf-dev libnetcdff-dev git
```

Compile with:

```
git clone https://github.com/Aida-Alvera/DINEOF
cd DINEOF/
cp config.mk.template config.mk
make
```

You might want to adapt `config.mk`, but the provided template `config.mk.template` should work with ubuntu as-is.

## Windows

### Windows Subsystem for Linux

Install "Windows Subsystem for Linux"

* Follow the instructions at https://aka.ms/wslinstall
* Install "Ubuntu" from the Windows App Store
* Follow the Ubuntu instructions

### Cygwin

* Use setup.exe to install the dependencies: gcc-fortran, make, libarpack-devel, liblapack-devel, libnetcdf-fortran-devel, git


```
git clone https://github.com/Aida-Alvera/DINEOF
cd DINEOF/
cp config.mk.template config.mk
make
```

For Cygwin, `OS` in `config.mk` should be `Linux` (default).
