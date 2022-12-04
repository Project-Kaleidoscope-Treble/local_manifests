1. Initial your repo repository as described by OFFICIAL Project Kaleidoscope
2. Clone this into `.repo/local_manifests` BEFORE syncing your Kaleidoscope source
3. `cd` to `device/phh/treble` and execute the `generate.sh` script
4. Launch the target you want and build it!
```
. build/envsetup.sh
lunch treble_arm64_avN-userdebug
WITHOUT_CHECK_API=true make -j$(nproc) systemimage
```
5. If you want to compress the system image after build finishes, go to out/target/product/phh_*/ folder and run
```
xz -9 -T0 -v -z system.img
```
