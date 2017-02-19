# How to build

Every cmake command must be executed inside the Build directory.

## Windows (MinGW)

Please see the BUILD_WINDOWS.md file in the IBMulator repository.

## Linux

### Debug
```
$ cmake -G "Unix Makefiles" -DCMAKE_CXX_FLAGS="-g -O0" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX:PATH=/absolute/path/to/debug
$ make & make install
```

### Release
```
$ cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX:PATH=/absolute/path/to/release
$ make & make install
```
