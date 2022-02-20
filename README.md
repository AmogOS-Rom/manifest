<p align="center">
</p>

Amog OS SUS Release
===========
AmogOS is the most SUS rom ever made, This is a fork from AEX.

Credits
-------
* [**AEX**](https://github.com/aospextended)
* [**JDCTeam**](https://github.com/AOSP-JF-MM)
* [**DirtyUnicorns**](https://github.com/DirtyUnicorns)
* [**TeamSubstratum (Theme Engine)**](https://github.com/Substratum)
* [**LineageOS/Cyanogenmod**](https://github.com/LineageOS)
* [**Nitrogen Project**](https://github.com/nitrogen-project)
* [**ABC ROM**](https://github.com/ezio84)
* [**GZOSP**](https://github.com/GZOSP)
* [**Pure Nexus**](https://github.com/PureNexusProject)
* [**OmniROM**](https://github.com/omnirom/)
* [**AOSPA**](https://github.com/aospa/)
* [**BlissRoms**](https://github.com/BlissRoms)

How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a 
command like this:

```bash
repo init -u git://github.com/AmogOS-Rom/manifest.git -b sus
```
To initialize a shallow clone, which will save even more space & time, use a command like this:

```bash
repo init --depth=1 -u git://github.com/AmogOS-Rom/manifest.git -b sus
```

Then to sync up:
----------------

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
Finally to build:
-----------------

```bash
source build/envsetup.sh
lunch aosp_device_codename-userdebug
make bacon -j$(nproc --all) | tee log.txt
```
