## to use ecl_offline
```
cd ecl_offline
git checkout px4v1.8.2
cd EKF
mkdir Build/
cd Build/
cmake ..
make

./myekf2

```
## use other version ecl
1.
```
cd EKF
cp CMakeLists.txt Myekf2.cpp myekf2.h ${OTHER_VERSION_ECL}/

```
tips:
 dont forget copy matrix to root directory${OTHER_VERSION_ECL}

## Prerequisites
origin from https://github.com/AbnerCSZ/EKF2_offline.git



# ECL

**Very lightweight Estimation & Control Library.**

[![DOI](https://zenodo.org/badge/22634/PX4/ecl.svg)](https://zenodo.org/badge/latestdoi/22634/PX4/ecl) [![Build Status](http://ci.px4.io:8080/buildStatus/icon?job=ecl/master)](http://ci.px4.io:8080/blue/organizations/jenkins/ecl/activity)

This library solves the estimation & control problems of a number of robots and drones. It accepts GPS, vision and inertial sensor inputs. It is extremely lightweight and efficient and yet has the rugged field-proven performance.

The library is BSD 3-clause licensed.



## EKF Documentation

  * [EKF Documentation and Tuning Guide](https://dev.px4.io/en/tutorials/tuning_the_ecl_ekf.html)

## Building EKF

### Prerequisites:

  * Matrix: A lightweight, BSD-licensed matrix math library: https://github.com/px4/matrix - it is automatically included as submodule.


By following the steps mentioned below you can create a shared library which can be included in projects using `-l` flag of gcc:

```
mkdir Build/
cd Build/
cmake ../EKF
make
```

Alternatively, just run:

```
./build.sh
```
