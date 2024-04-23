# XT-CORE release 0.1.0

## Summary

This release v0.1.0 is the first attempt to apply new release strategy and to organize core xen-troops projects into the xt-core entity.

This release fixes current state of the mentioned below projects and projects used by entities included into the release.

Release allows to build xen-based project for some Renesas R-Car S4, H3 and M3 boards with the following components:
- loaders (Arm trusted firmware, optee-os, u-boot)
- xen
- Dom0 as hardware-less control domain
- DomD as the driver domain
- DomU as the guest with Linux OS (optionally)
- DomA with Android OS (optionally)
- DomZ with Zephyr OS (optionally)

Release of the xt-core itself is not intended to be used alone, but provides required functionality and tunning for the products based on it.

Projects meta-xt-prod-devel-rcar, meta-xt-prod-devel-rcar-gen4, meta-aos-rcar-gen3 and meta-aos-rcar-gen4 should be used as the reference software, that can create ready to use products.

## Content of the release

- meta-xt-common https://github.com/xen-troops/meta-xt-common
- meta-xt-rcar https://github.com/xen-troops/meta-xt-rcar
- meta-xt-vhost https://github.com/xen-troops/meta-xt-vhost

Release is done on the following branches:
- master (kirkstone). On this branch release tag is `v0.1.0`.
- dunfell for meta-xt-common and meta-xt-rcar. On this branch release tag is `dunfell-v0.1.0`.

Release commits are:
- meta-xt-common master branch - [7919053015dd323f725ec50ff01ac8fe7c61530a](https://github.com/xen-troops/meta-xt-common/commit/7919053015dd323f725ec50ff01ac8fe7c61530a)
- meta-xt-common dunfell branch - [6dcc99c28625b92ed4f159c34e8c41b92df27dba](https://github.com/xen-troops/meta-xt-common/commit/6dcc99c28625b92ed4f159c34e8c41b92df27dba)
- meta-xt-rcar master branch - [b0d71b808e8d9b545abce3ebd806864d6eba840d](https://github.com/xen-troops/meta-xt-rcar/commit/b0d71b808e8d9b545abce3ebd806864d6eba840d)
- meta-xt-rcar dunfell branch - [f941326e1477961e7725b5bbdf2f4cb952d507fc](https://github.com/xen-troops/meta-xt-rcar/commit/f941326e1477961e7725b5bbdf2f4cb952d507fc)
- meta-xt-vhost - [5fc85dbf9aafe3f74ef0cd022811d0a73144a675](https://github.com/xen-troops/meta-xt-vhost/commit/5fc85dbf9aafe3f74ef0cd022811d0a73144a675)

Example of usage of xt-core v0.1.0 in yaml file for the moulin:
```
- type: git
  url: https://github.com/xen-troops/meta-xt-common.git
  rev: v0.1.0
- type: git
  url: https://github.com/xen-troops/meta-xt-rcar.git
  rev: v0.1.0
- type: git
  url: https://github.com/xen-troops/meta-xt-vhost.git
  rev: v0.1.0
```

## List of the sub-repositories used by this release

### meta-xt-common branch master (kirkstone)

| component | repo and commit |
| - | - |
| linux 6.8.0-rc1 | https://github.com/torvalds/linux/commit/6613476e225e090cc9aad49be7fa504e290dd33d |
| displaymanager | https://github.com/xen-troops/DisplayManager/commit/868e703b7652c9a40ae878d7d517f97398b4549c |
| camerabe | https://github.com/xen-troops/camera_be/commit/b12d4934b7d3fed75d1255793893070768636555 |
| virtio-disk | https://github.com/xen-troops/virtio-disk/commit/274f5e933a7381a9eb2a7b5856f37c3d982f3874 |
| libxenbe | https://github.com/xen-troops/libxenbe/commit/21f1fdc090ee5342df7608358c5130a7675dad68 |
| displbe | https://github.com/xen-troops/displ_be/commit/b218acf44e71c4a77082944e3878e1859a352fba |
| sndbe | https://github.com/xen-troops/snd_be/commit/b2764c2849f02c051f1d16dc6b592da59d1675c1 |
| xt-log | https://github.com/xen-troops/xt-log/commit/a88163b7f64c4eec4f7362ba33ecd55bd3dd1cdb |
| optee-test 4.1.0 | https://github.com/OP-TEE/optee_test/commit/2e1e7a9c9d659585566a75fc8802f4758c42bcb2 |
| optee-client 4.1.0 | https://github.com/OP-TEE/optee_client/commit/f7e4ced15d1fefd073bbfc484fe0e1f74afe96c2 |
| optee-os 4.1.0 | https://github.com/OP-TEE/optee_os/commit/18b424c23aa5a798dfe2e4d20b4bde3919dc4e99 |
| optee-examples 4.1.0 | https://github.com/linaro-swg/optee_examples/commit/378dc0db2d5dd279f58a3b6cb3f78ffd6b165035 |
| wayland-ivi-extension | https://github.com/COVESA/wayland-ivi-extension/commit/f6911a11dc911a5bcb380d0895db6cfd533a3569 |
| dbus-cxx 0.10.0 | https://github.com/dbus-cxx/dbus-cxx/commit/1d9425027860d5b9006178aefc2e638c48848477 |
| xen 4.16 | https://github.com/xen-troops/xen/commit/81ac624282e6ab429dfdb858da8360faf45ca8d7 |
| qemu 7.0.0 | https://github.com/xen-troops/qemu/commit/5456c82c966570c1a64524cd3fb7116d80199500 |
| u-boot-android-bazel | https://github.com/xen-troops/android_u-boot_manifest/commit/30adce0c709887d9788f33b494ae79090b8bcc17 |


### meta-xt-common branch dunfell

| component | repo and commit |
| - | - |
| linux 5.10.41 | https://github.com/xen-troops/linux/commit/d7c1b717e3f11b6aa0713dcefa8cf1ed4c1222af |
| displaymanager | https://github.com/xen-troops/DisplayManager/commit/868e703b7652c9a40ae878d7d517f97398b4549c |
| camerabe | https://github.com/xen-troops/camera_be/commit/b12d4934b7d3fed75d1255793893070768636555 |
| virtio-disk | https://github.com/xen-troops/virtio-disk/commit/327f4cfa1d016b85b59366ef1ad53e1f734d1e2f |
| libxenbe | https://github.com/xen-troops/libxenbe/commit/21f1fdc090ee5342df7608358c5130a7675dad68 |
| displbe | https://github.com/xen-troops/displ_be/commit/b218acf44e71c4a77082944e3878e1859a352fba |
| sndbe | https://github.com/xen-troops/snd_be/commit/b2764c2849f02c051f1d16dc6b592da59d1675c1 |
| xt-log | https://github.com/xen-troops/xt-log/commit/a88163b7f64c4eec4f7362ba33ecd55bd3dd1cdb |
| wayland-ivi-extension | https://github.com/COVESA/wayland-ivi-extension/commit/e9c2fe4c5034a06b159cfd45dbd485755cbaf4c8 |
| dbus-cxx 0.10.0 | https://github.com/dbus-cxx/dbus-cxx/commit/1d9425027860d5b9006178aefc2e638c48848477 |
| xen 4.16 | https://github.com/xen-troops/xen/commit/81ac624282e6ab429dfdb858da8360faf45ca8d7 |
| u-boot-android | https://github.com/xen-troops/u-boot/commit/6009039b25411bb567b5394de56f79256e71cfc8 |


### meta-xt-rcar branch master (kirkstone)

| component | repo and commit |
| - | - |
| Imagination DDK 1.11 UM | https://gitpct.epam.com/epmd-aepr/pvr_um_vgpu_img/commit/4ed61e604d925bfce8ab16645f48425a581496c7 |
| Imagination DDK 1.15 UM | https://gitpct.epam.com/epmd-aepr/pvr_um_vgpu_img/commit/e172e94c7d61186fe5b64db68fdef949c9ee2189 |
| Imagination DDK 1.11 KM | https://gitpct.epam.com/epmd-aepr/pvr_km_vgpu_img/commit/6994a4be87075975665fcef1fd95c087b0a007c8 |
| Imagination DDK 1.15 KM | https://gitpct.epam.com/epmd-aepr/pvr_km_vgpu_img/commit/487a9326d5446bf4ed2808980ab0b12d8fd3f9e9 |
| optee-os 3.9 | https://github.com/xen-troops/optee_os/commit/192b616c9715604a2d2b16bc61758d160550806e |
| optee-test 3.9 | https://github.com/OP-TEE/optee_test/commit/21b347a3d75fd52fd49130e75c962c5b56123d2f |
| linux 5.10.41 rcar-gen3 | https://github.com/xen-troops/linux/commit/bf7d6bcdd618e5acb21118d87c76e5d8913f8dde |
| linux 5.10.41 rcar-gen4 | https://github.com/xen-troops/linux/commit/769ab722739878c3c1aaa1571f6ca996b135f8f6 |

### meta-xt-rcar branch dunfell

| component | repo and commit |
| - | - |
| Imagination DDK 1.11 UM | https://gitpct.epam.com/epmd-aepr/pvr_um_vgpu_img/commit/4ed61e604d925bfce8ab16645f48425a581496c7 |
| Imagination DDK 1.11 KM | https://gitpct.epam.com/epmd-aepr/pvr_km_vgpu_img/commit/6994a4be87075975665fcef1fd95c087b0a007c8 |
| optee-os 3.9 | https://github.com/xen-troops/optee_os/commit/192b616c9715604a2d2b16bc61758d160550806e |
| optee-test 3.13 | https://github.com/OP-TEE/optee_test/commit/21b347a3d75fd52fd49130e75c962c5b56123d2f |
| linux 5.10.41 rcar-gen3 | https://github.com/xen-troops/linux/commit/d7c1b717e3f11b6aa0713dcefa8cf1ed4c1222af |
| linux 5.10.41 rcar-gen4 | https://github.com/xen-troops/linux/commit/769ab722739878c3c1aaa1571f6ca996b135f8f6 |


## Variables required to be set by the product

Note that `%{SOMETHING}` represents some value that is defined by the product and is transferred into `xt-core` through yocto variables.

See the following yaml-files as working reference examples.
For PV-based configuration - https://github.com/xen-troops/meta-xt-prod-devel-rcar/blob/master/prod-devel-rcar.yaml
For virtio-based configuration - https://github.com/xen-troops/meta-xt-prod-devel-rcar/blob/master/prod-devel-rcar-virtio.yaml

### Variables required to be set for Dom0
```
MACHINE = "%{DOM0_MACHINE}"
XT_DOMD_CONFIG_NAME = "%{XT_DOMD_CONFIG_NAME}"
XT_DOMD_DTB_NAME = "%{XT_DOMD_DTB_NAME}"
XT_DOM_NAME = "dom0"
XT_GUEST_INSTALL = "domd %{XT_GENERIC_DOMU_TAG} %{XT_DOMA_TAG} %{XT_DOMZ_TAG}"
INIT_MANAGER = "systemd"
```

If Linux as guest domain is present
```
XT_GENERIC_DOMU_TAG = "domu"
XT_DOMU_DTB_NAME = "%{XT_DOMU_DTB_NAME}"
XT_DOMU_CONFIG_NAME = "%{XT_DOMU_CONFIG_NAME}"
```

If Android as guest domain is present
```
XT_DOMA_TAG = "doma"
XT_DOMA_DTB_NAME = "%{XT_DOMA_DTB_NAME}"
XT_DOMA_CONFIG_NAME = "%{XT_DOMA_CONFIG_NAME}"
OVERRIDES:append = ":enable_android"
```

If Zephyr as guest domain is present
```
XT_DOMZ_TAG = "domz"
XT_DOMZ_CONFIG_NAME = "%{XT_DOMZ_CONFIG_NAME}"
```

### Variables required to be set for DomD
```
MACHINE = "%{DOMD_MACHINE}"
XT_DOM_NAME = "domd"
XT_OP_TEE_FLAVOUR = "%{XT_OP_TEE_FLAVOUR}"
XT_DEVICE_TREES = "%{XT_DOMD_DTB_NAME} %{XT_DOMA_DTB_NAME} %{XT_XEN_DTB_NAME}"
XT_GUEST_INSTALL = "%{XT_GENERIC_DOMU_TAG} %{XT_DOMA_TAG} %{XT_DOMZ_TAG}"
```

If Multimedia is used for the R-Car Gen3.
These variables are used inside xt-core just
to prepare Renesas proprietary multimedia packages.
These packages are not a part of the xt-core release
and have to be obtained from the Renesas.
```
XT_MULTIMEDIA_EVA_DIR = "%{XT_MULTIMEDIA_EVA_DIR}"
"HOSTTOOLS:append" = " unzip "
```

If DomA is present
```
DISTRO_FEATURES:append = " ivi-shell"
```

If R-Car Gen3 prebuilt graphic packages are used.
These packages are not a part of the xt-core release
and have to be obtained from the Renesas.
```
XT_PVR_NUM_OSID = "%{XT_PVR_NUM_OSID}"
DISTRO_FEATURES_NATIVESDK:append = " wayland"
DISTRO_FEATURES:append = " pam"
MACHINE_FEATURES:append = " gsx"
BB_MULTI_PROVIDER_ALLOWED:append," virtual/libgl virtual/egl virtual/libgles1 virtual/libgles2"
PREFERRED_PROVIDER_virtual/libgles1 = ""
PREFERRED_PROVIDER_virtual/libgles2 = "gles-user-module"
PREFERRED_PROVIDER_virtual/libgles3 = "gles-user-module"
PREFERRED_PROVIDER_virtual/egl = "libegl"
PREFERRED_PROVIDER_virtual/libgl = ""
PREFERRED_PROVIDER_virtual/mesa = ""
PREFERRED_PROVIDER_virtual/libgbm = "libgbm"
PREFERRED_PROVIDER_libgbm-dev = "libgbm"
BBMASK:append = " mesa-gl"
XT_USE_DDK1_11 = "%{XT_USE_DDK1_11}" ## should be set to 1 (DDK 1.11) or 0 (DDK 1.15)
XT_PREBUILT_GSX_DIR = "%{XT_PREBUILT_GSX_DIR}"
```


### Variables required to be set for DomU
```
MACHINE = "%{DOMU_MACHINE}"
XT_DOM_NAME = "domu"
```

If R-Car Gen3 prebuilt graphic packages are used.
These packages are not a part of the xt-core release
and have to be obtained from the Renesas.
```
XT_PVR_NUM_OSID = "%{XT_PVR_NUM_OSID}"
DISTRO_FEATURES_NATIVESDK:append = " wayland"
DISTRO_FEATURES:append = " pam"
MACHINE_FEATURES:append = " gsx"
BB_MULTI_PROVIDER_ALLOWED:append," virtual/libgl virtual/egl virtual/libgles1 virtual/libgles2"
PREFERRED_PROVIDER_virtual/libgles1 = ""
PREFERRED_PROVIDER_virtual/libgles2 = "gles-user-module"
PREFERRED_PROVIDER_virtual/libgles3 = "gles-user-module"
PREFERRED_PROVIDER_virtual/egl = "libegl"
PREFERRED_PROVIDER_virtual/libgl = ""
PREFERRED_PROVIDER_virtual/mesa = ""
PREFERRED_PROVIDER_virtual/libgbm = "libgbm"
PREFERRED_PROVIDER_libgbm-dev = "libgbm"
BBMASK:append = " mesa-gl"
XT_USE_DDK1_11 = "%{XT_USE_DDK1_11}" ## should be set to 1 (DDK 1.11) or 0 (DDK 1.15)
XT_PREBUILT_GSX_DIR = "%{XT_PREBUILT_GSX_DIR}"
```
