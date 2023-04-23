ShirayukiProject
====================

How to Build?
-------------

To initialize your local repository, use a 
command like this:

```bash
repo init -u https://github.com/shirayuki-prjkt/yuki_manifest.git -b tsushima-13
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
lunch aosp_$device-userdebug
```

Build it:
----------------

```bash
mka bacon -jX
```

----------------

Add some configuration in
your device trees:

Default build type is Vanilla
If you want build with PixelExperience GApps, add this in your device.mk

PIXEL_GAPPS := true

If you want to build vanilla, don't set this

-----------------

Define your bootanimation res by using

TARGET_BOOT_ANIMATION_RES := (res)

res can be 1080 and 1440 (720 will be added soon)

------------------

