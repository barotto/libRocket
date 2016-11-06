# How to build

Every cmake command must be executed inside the Build directory.

## Windows (MinGW)

To build libRocket with MinGW 64 (not the MSYS shell) you'll need:
* freetype in the libRocket/Dependencies directory
* libz.a in the freetype/lib directory
* cmake in the PATH env variable
* MinGW 64 bin directory in the PATH env variable

$ cmake -G "MinGW Makefiles" -DCMAKE_MAKE_PROGRAM="c:\mingw64\bin\mingw32-make.exe" -DFREETYPE_INCLUDE_DIRS="..\Depencencies\freetype\include;..\Dependencies\freetype\include\freetype2" -DFREETYPE_LIBRARY="..\Dependencies\freetype\lib\libfreetype.a;..\Dependencies\freetype\lib\libz.a"
$ mingw32-make

For more info see how_to_build_for_mingw.txt

To compile freetype in MSYS shell go inside the freetype directory and:
$ ./configure --host=x86_64-w64-mingw32 --build=x86_64-w64-mingw32

## Linux

### Debug
$ cmake -G "Unix Makefiles" -DCMAKE_CXX_FLAGS="-g -O0" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX:PATH=/absolute/path/to/debug
$ make & make install

### Release
$ cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX:PATH=/absolute/path/to/release
$ make & make install

