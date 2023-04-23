ShirayukiProject
====================

How to Build?
-------------

To initialize your local repository, use a 
command like this:

```bash
repo init -u https://github.com/shirayuki-prjkt/yuki_manifest.git -b tsunemori-13
```

Then to sync up:
----------------

```bash
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```

Setting up build environment:
----------------

```bash
. build/envsetup.sh
```

Lunch:
----------------

```bash
lunch shirayuki_<device_name>-userdebug
```

Build it:
----------------

```bash
mka shirayuki
```

----------------

Add some configuration in
your device trees:

If you want build with GApps, add this in your device.mk

TARGET_GAPPS_ARCH := (arch)

arch can be arm, arm64, x86_64, or x86
If you want to build vanilla, don't set this

-----------------

If you want to add Lawnchair, add this in your device.mk

USE_LAWNCHAIR := true

-----------------

Define your bootanimation res by using

TARGET_BOOT_ANIMATION_RES := (res)

res can be 720, 1080, or 1440

------------------

