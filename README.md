# Sensu Go Asset Utilities

## Overview

DON'T JUDGE ME.

## Usage

```
create-sensu-asset -h
NAME
  create-sensu-asset -- creates Sensu Go asset packages (tarballs).

SYNOPSIS
  create-sensu-asset -a ASSET_NAME -v ASSET_VERSION -b /path/to/executable/script/or/binary

DESCRIPTION
  The create-sensu-asset utility builds Sensu 2 assets containing
  /bin /lib and /include subdirectories, copying the user-
  provided -b BINARY -l LIBRARIES -i INCLUDES files, and
  compressing them as a gzipped tarball.

  The options are as follows:

  -h      Prints this help!
  -a ASSET_NAME
          The asset package file name prefix (i.e. tarball file
          name). REQUIRED
  -v ASSET_VERSION
          The asset package file name suffix (i.e. the tarball
          file name suffix). OPTIONAL
  -b BINARIES
          The path(s) to executable scripts or binary files,
          which will be packaged in the asset /bin directory, and
          added to the Sensu Agent $PATH environment variable at
          runtime. Multiple files may be specified as a
          comma-separated list. OPTIONAL
  -l LIBRARIES
          The path(s) to linked library files, which will be
          packaged in the asset /lib directory, and added to the
          Sensu Agent $LD_LIBRARY_PATH environment variable at.
          runtime. Multiple files may be specified as a comma-
          separated. OPTIONAL
  -i INCLUDES
          The path(s) to any additional files, which will be
          packaged in the asset /include directory and accessible
          Multiple files may be specified as a comma-separated
          list. OPTIONAL
  -e EXTRA
          The path(s) to any additional files or directories,
          which will be packaged in the asset / (root) directory.
          Multiple files or directories may be specified as a
          comma-separated list. OPTIONAL
  -o OUTPUT_DIR
          The directory where the asset should be created
          (output). Defaults to $PWD
```
