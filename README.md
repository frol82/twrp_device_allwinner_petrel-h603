# X96H-QUAD-CORE-TWRP

First checkout minimal twrp with omnirom tree: 
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0 
repo sync

cd /***/twrp-9.0 
export ALLOW_MISSING_DEPENDENCIES=true 
export LC_ALL=C ccache -C 
. build/envsetup.sh 
lunch omni_petrel_h603-eng 
make -j8 recoveryimage
