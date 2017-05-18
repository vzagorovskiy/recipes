# Install GDAL for Windows
## Install Visual C++ 2015 Build Tools
* Download Visual C++ 2015 Build Tools from http://landinghub.visualstudio.com/visual-cpp-build-tools
* Install Visual C++ 2015 Build Tools

## Download and install GDAL
1. Download GDAL sources from http://download.osgeo.org/gdal/CURRENT/
1. Unzip downloaded file gdalXXX.zip to /sources/gdal-X.X.X directory
1. Edit nmake.opt in /sources/gdal-X.X.X directory
    - MSVC_VER=1900
    - GDAL_HOME = "c:\gdal"
1. Set system environment variables
    - GDAL_DATA = c:\gdal\data
    - add c:\gdal\bin to PATH 
1. Run cmd and execute following commands
    - cd /sources/gdal-X.X.X
    - "%VS140COMNTOOLS%vsvars32.bat"
    - nmake /f makefile.vc
    - nmake /f makefile.vc devinstall

## Install PROJ.4
1. Download PROJ.4 from http://proj4.org/download.html#current-release or from GitHub https://github.com/OSGeo/proj.4
1. Set system environment variables
    - PROJ_LIB = c:\proj
## Install GDAL for Python
    
