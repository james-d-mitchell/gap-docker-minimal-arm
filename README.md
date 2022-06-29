# Docker container for the core GAP system

The Docker container for the core GAP system is available at DockerHub here:
https://hub.docker.com/r/jamesdbmitchell/gap-docker-minimal-arm

This GAP Docker container provides only the core GAP system and several packages
which are needed by GAP (PackageManager, GAPDoc, PrimGrp, SmallGrp, TransGrp).
It may be used, for example, in automated tests of different configurations of
GAP packages by installing them in the `pkg` subdirectory of
`/home/gap/inst/gap-4.X.Y/`. 

If you install Docker, you may run GAP in this container interactively.

```
$ docker run --rm -i -t jamesdbmitchell/gap-docker-minimal-arm:version-4.11.0
gap@929a1967856a:~$ gap -A
 *********   GAP 4.11.0 of 29-Feb-2020
 *  GAP  *   https://www.gap-system.org
 *********   Architecture: aarch64-unknown-linux-gnu-default64-kv7
 Configuration:  gmp 6.2.0, GASMAN, readline
 Loading the library and packages ...
 Packages:   GAPDoc 1.6.4, PrimGrp 3.4.1, SmallGrp 1.4.2, TransGrp 3.1
 Try '??help' for help. See also '?copyright', '?cite' and '?authors'
gap>
```
