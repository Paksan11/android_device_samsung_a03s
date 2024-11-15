## Recovery Device Tree for the Samsung Galaxy A03S (MTK)

## How-to compile it:

# Create dirs
$ mkdir tw; cd tw

# Init repo
$ repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1

# Clone a03s repo
$ git clone https://github.com/Paksan11/android_device_samsung_a03s device/samsung/a03s

# Clone a03s kernel


# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a03s-eng; mka recoveryimage

# Disable File Based Encryption (FBE) after installing TWRP.
not implemented


Blobs version:
> Kernel base: Compiled from source.