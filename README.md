# codeblocks_custom_build

The plan is to do these steps to the Code::Blocks newest SVN.

## 1. Normalize line-feeds
###a. Create src/.gitattributes file
###b. Normalize line-feeds on Windows
###c. Add src/.gitattributes file

## 2. Delete obsolete files from repo
###a. Remove win32 wxWidgets template files
###b. Delete files: src/ipc.cpp and src/ipc.h
###c. Remove obsolete CB projects codecompletion.cbp and wxpropgrid.cbp

## 3. Fix Portablity Issues
###a. Remove Windows stuff from Unix CB projects
###b. Save-As Windows wx2.8 32 bit projects
###c. Save-As Windows wx3.0 64 bit projects
###d. Add missing compiler option "-std=gnu++11"
###e. Fix SpellChecker windows projects issues
###f. Fix wxSmithDemo.cbp project issues
###g. Fix TestPlot.cbp project issues
###h. Add WX_VERSION=28
###i. Change library prefix from "wxmsw28" to "wxmsw$(WX_VERSION)"
###j. Add WX_COMPILER="gcc" and WX_TOOLKIT="msw"
###k. Change "gcc_dll" to "$(WX_COMPILER)_dll"
###l. Move wxmsw$(WX_VERSION)$(WX_SUFFIX) to target level

## 4. Change to using lib, lib28, or lib30 folders
###a. Add src/.gitignore
###b. Edit the old .gitignore
###c. Change Linux CB Projects to have ".a" files in lib?? folders
###d. Change Windows CB Projects to have ".a" files in lib?? folders

## 5. Change simple source code issues related to branding
###a. Add SDK header "branding.h"
###b. Add use of STANDARD_DATA_PATH like used in Em::Blocks
###c. Add use of APP_NAME partly like used in Em::Blocks

## 6. Fix PCH Issues
###a. Fix PCH Issues on Linux when using CB Projects
###b. Fix PCH Issues on Windows

## 7. Change CB Projects to NOT use update batch or script files
###a. Change Linux CB Projects
###b. Change Windows CB Projects
