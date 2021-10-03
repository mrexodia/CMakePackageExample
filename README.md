# CMakePackageExample

Attempt to set up a good CMake packaging example.

## Building

First you need to build and install `ClimbingStats`:

```sh
cd ClimbingStats
cmake -B build
cmake --build build
cmake --install build --prefix install
```

Then you build `MainApp`:

```sh
cd ../MainApp
cmake -B build -DCMAKE_PREFIX_PATH=$(pwd)/../ClimbingStats/install
cmake --build build
build/MainApp
```