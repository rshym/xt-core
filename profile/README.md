# Welcome to Xen-Troops!

We develop embedded automotive Xen for different hardware platforms and actively contribute to Xen, Linux, OPTEE, Zephyr, and other communities.

---
## Where to start

### Build system
Due to the complex nature of our products and the need to build different OS, we use [moulin](https://github.com/xen-troops/moulin) build system which allows us to build systems containing different OS (Linux, Zephyr, Android) with inter-domain dependencies.

The human-friendly YAML files describe a whole multi-domain system with build entities and configurations.

Documentation with examples and hints is available on the [moulin.readthedocs.io](https://moulin.readthedocs.io/).

### Products
We have a few actively developing public reference products:

[meta-xt-prod-devel-rcar](https://github.com/xen-troops/meta-xt-prod-devel-rcar)
- Renesas R-Car Gen3 with 8GB
- with PV- and virtio-based configurations
- GPU sharing between domains
- Linux-based Dom0 (control domain)
- Linux-based DomD (driver domain) and DomU
- Graphics back-end in DomD
- Networking in DomD, DomU and DomA (Android)
- Network (NFS) boot for DomD and DomU
- OP-TEE client in DomU
- Virtualized OP-TEE build
- ARM-TF that boots into EL2
- Multimedia (HW-assisted video decoding/encoding) support
- SD or eMMC boot
- Android VM support
- Zephyr OS as guest
  
[meta-xt-prod-devel-rcar-gen4](https://github.com/xen-troops/meta-xt-prod-devel-rcar-gen4) for Renesas R-Car Gen4
- Renesas R-Car Gen4
- Thin Dom0
- Driver domain (DomD), which has access to all available hardware
- Optional generic domain (DomU)
- Support for OP-TEE in virtualization mode
- ICCOM partitioning demo (proprietary components are required to test the feature)
- R-Switch VMQ: R-Switch virtualization feature
- R-Switch VMQ TSN: R-Switch TSN pass-through feature
- R-Switch L3 routing offload (including VLAN routes)
- R-Switch traffic control offload
- R-Switch offloaded IPS/IDS Snort support
- Disabling L3 HW forwarding respectively to /proc/sys/net/ipv4/ip_forward value
- Disabling/enabling L3 offload via sysfs file
- PCIe SR-IOV support

### Core components
All our products are based on the top of the 'xt-core' that provides base components, such as backends, and pre-configuration for things like linux, u-boot, xen, ATF, qemu etc.

Base platform `xt-core` is split into hardware independent and hardware-specific parts.
- [meta-xt-common](https://github.com/xen-troops/meta-xt-common) - hardware independent components
- [meta-xt-rcar](https://github.com/xen-troops/meta-xt-rcar) - and platform-specific things for Renesas R-Car platform
- meta-xt-rpi5 is under active development now

---
## Releases

### Products
Products are realesed according to their road map.
Available releases can be found at
- [meta-xt-prod-devel-rcar](https://github.com/xen-troops/meta-xt-prod-devel-rcar/releases)
- [meta-xt-prod-devel-rcar-gen4](https://github.com/xen-troops/meta-xt-prod-devel-rcar-gen4/releases)


### xt-core
xt-core has it's own line of releases
- [meta-xt-common](https://github.com/xen-troops/meta-xt-common/releases)
- [meta-xt-rcar](https://github.com/xen-troops/meta-xt-rcar/releases)
