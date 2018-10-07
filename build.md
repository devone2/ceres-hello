# Building

Dependencies:
 - ceres-solver
 - eigen
 
Transitive dependencies:
 - ceres-solver:
   - eigen
   - glog
 
For initial cmake configuration we need to set paths to dependencies. We use nonstandard location for both dependencies in docker container:
```
/home/controller/3rdParty_REPO_gcc5.4.0/
```

For building in container:
```
cd ~/ceres/ceres-hello/

mkdir build
cmake ../ -DEIGEN_INCLUDE_DIR=~/3rdParty_REPO_gcc5.4.0/Eigen-3.2.9/ -DCMAKE_PREFIX_PATH=~/3rdParty_REPO_gcc5.4.0/ceres-solver-1.12.0/
make
```
