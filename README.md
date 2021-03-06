# OpenXT manifest

Simple manifest to play around with OpenXT using repo instead of the proposed
build systems. This aims to provide a more direct and simple way to build the
project without relying on a specific container technology or imposing changes
in one's work-flow.

## Manifests

### default.xml

Development manifest.

* OpenXT: master branch;
* Bitbake: tag 1.34;
* OpenEmbedded-core & meta-Openembedded: pyro branch;
* meta-intel, meta-java, meta-virtualization: pyro branch;
* meta-selinux: master branch;

### stable-8

Stabilisation manifest for 8.x releases.

* OpenXT: stable-8 branch;
* Bitbake: tag 1.34;
* openembedded-core: revision 819aa151bd634122a46ffdd822064313c67f5ba5;
* meta-openembedded: revision 9eaebc6e783f1394bb5444326cd05a976b3122e9;
* meta-intel: revision 9b37952d6af36358b6397cedf3dd53ec8962b6bf;
* meta-java: revision 0c27b120aa508e4bb41394b8dd3645949a611128;
* meta-virtualization: revision 45ad257a1e4a6707c376d2f7eb26c3c8bdf03607;
* meta-selinux: revision d855c624f32c5e599bf27e06cb8f5b25b3aae12d;

### stable-7

Stabilisation manifest for 7.x releases.

* OpenXT: stable-7 branch;
* Bitbake: revision 68d061d2517f1a79dc6b14a373ed2dcb78a901ce;
* openembedded-core: revision 6af6e285e8bed16b02dee27c8466e9f4f9f21e30;
* meta-openembedded: revision 2ea8d7f54a061e902657c4f8ea1f7f7c25c6c4e1;
* meta-intel: revision 4e8b0ef1e521dc45dcc310b6b7528bfe1eed1274;
* meta-java: revision a73939323984fca1e919d3408d3301ccdbceac9c;
* meta-virtualization: revision 042425c1d98bdd7e44a62789bd03b375045266f5;
* meta-selinux: revision 4c75d9cbcf1d75043c7c5ab315aa383d9b227510;

### stable-6

Stabilisation manifest for 6.x releases.

* OpenXT: stable-6 branch;
* Bitbake: revision b993d96203541cd2919d688559ab802078a7a506;
* openembedded-core: revision 1f4bfa33073584c25396d74f3929f263f3df188b;
* meta-openembedded: revision 8ab04afbffb4bc5184cfe0655049de6f44269990;
* meta-java: revision a73939323984fca1e919d3408d3301ccdbceac9c;
* meta-selinux: revision 4c75d9cbcf1d75043c7c5ab315aa383d9b227510;
