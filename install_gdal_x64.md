https://stackoverflow.com/questions/16526181/cant-build-gdal-in-x64

1.	If you tried to build GDAL previously (e.g. x86), make sure that the build directory (C:\gdal\bin) and the source directory are clean from previous build attempt. If unsure, try to unpack sources in a new directory.
2.	Start VS2015 x64 Native Tools Command Prompt: Start -> All Programs -> Microsoft Visual Studio 2015 -> Visual Studio Tools -> Open VS2015 x64 Native Tools Command Prompt
Or run %comspec% /k "C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\vcvarsall.bat" amd64).
3.	Change directory to the directory with unpacked GDAL sources:
4.	C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC>cd /D C:\tmp\gdal-x.x.x
5.  D:\trn4\gdal-x.x.x>
6.	Build GDAL with development files:
7.	nmake /f makefile.vc MSVC_VER=1900 WIN64=YES
8.	nmake /f makefile.vc MSVC_VER=1900 WIN64=YES install
nmake /f makefile.vc MSVC_VER=1900 WIN64=YES devinstall
You can get your MSVC_VER number from here http://www.cmake.org/cmake/help/v3.0/variable/MSVC_VERSION.html. GDAL will be built and installed to C:\warmerda\bld\.
