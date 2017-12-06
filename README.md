# OpenXT manifest

Simple manifest to play around with OpenXT using repo instead of the proposed
build systems. This aims to provide a more direct and simple way to build the
project without relying on a specific container technology or imposing changes
in one's work-flow.

## Known issues with upstream repositories

* Problem with libtirpc
```
| src/rpcb_svc_com.o: In function `handle_reply':
| /home/build/openxt/master-0/tmp-glibc/work/core2-32-oe-linux/rpcbind/0.2.3-r0/rpcbind-0.2.3/src/rpcb_svc_com.c:1298: undefined reference to `svc_auth_none'
| collect2: error: ld returned 1 exit status
```
Addressed by https://github.com/eric-ch/xenclient-oe/commit/0c1ac3f682f0b7c67628c2c93e45eba9e164cb19

* OpenXT should add "multiarch" to DISTRO_FEATURES.
Addressed by https://github.com/eric-ch/xenclient-oe/commit/66625887c982e1133d455970227e7e6b18f5adf8

## Manifests
 
### pyro.xml

Manifest for the OpenXT upgrade to Pyro (Yocto 2.3).
This is still work in progress and uses forks of OpenXT upstream repositories.

#### Quirks and requirements

Some dependencies are still required on the host, usual dev tools aside some
are compatibility libraries required to have the native ghc6 compiler in the
native environment. Although an alternative approach would be to "require" ghc6
to be present and installed, it seems easier to provide a recipe. ghc6 being
quite old, building it using modern libraries and compilers will most likely
fail, so it is using the binary package provided by
https://www.haskell.org/ghc/download_ghc_6_12_3 (12 June 2010).
Writing recipes for the libraries would be just fine, and -native would be
generated by bitbake etc... but they are widely avaiable to most distributions
anyway.
Following are the Arch Linux package names:
- gcc-multilibs
- gcc-libs-multilib
- lib32-gcc-libs
- lib32-glibc
- lib32-gmp4 (AUR)
- lib32-ncurses5-compat-libs (AUR)
