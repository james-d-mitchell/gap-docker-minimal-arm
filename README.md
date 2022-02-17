# Docker container for the core GAP system

The Docker container for the core GAP system is available at DockerHub here:
https://hub.docker.com/r/jamesdbmitchell/gap-docker-minimal-arm

This GAP Docker container provides only the core GAP system and several packages
which are needed by GAP (PackageManager, GAPDoc, PrimGrp, SmallGrp, TransGrp).
It may be used, for example, in automated tests of different configurations of
GAP packages by installing them in the `pkg` subdirectory of
`/home/gap/inst/gap-4.X.Y/`. 

If you install Docker, you may run GAP in this container interactively. As you
see from the output below, it does not have a number of packages included in
the official GAP distribution. 

```
$ docker run --rm -i -t jamesdbmitchell/gap-docker-minimal-arm
gap@371f2d47a17d:~$ gap
 *********   GAP 4.10.2 of 19-Jun-2019
 *  GAP  *   https://www.gap-system.org
 *********   Architecture: aarch64-unknown-linux-gnu-default64-kv3
 Configuration:  gmp 6.2.0, readline
 Loading the library and packages ...
#I  autpgrp package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  alnuth package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  crisp package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  ctbllib package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  factint package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  fga package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  irredsol package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  laguna package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  polenta package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  polycyclic package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  resclasses package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  sophus package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
#I  tomlib package is not available. Check that the name is correct
#I  and it is present in one of the GAP root directories (see '??RootPaths')
 Packages:   GAPDoc 1.6.2, PrimGrp 3.3.2, SmallGrp 1.3, TransGrp 2.0.4
 Try '??help' for help. See also '?copyright', '?cite' and '?authors'
gap>
```
