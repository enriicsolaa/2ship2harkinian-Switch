# 2 Ship 2 Harkinian

### Playtesting
If you want to playtest a continuous integration build, you can find them at the links below. Keep in mind that these are for playtesting only, and you will likely encounter bugs and possibly crashes. 

* [Windows](https://nightly.link/HarbourMasters/2ship2harkinian/workflows/main/develop/2ship-windows.zip)
* [Linux](https://nightly.link/HarbourMasters/2ship2harkinian/workflows/main/develop/2ship-linux.zip)
* [Mac](https://nightly.link/HarbourMasters/2ship2harkinian/workflows/main/develop/2ship-mac.zip)

### Wii U Build
```bash
cmake --build build-cmake/ --target Generate2ShipOtr

cmake -H. -Bbuild-wiiu -GNinja -DCMAKE_TOOLCHAIN_FILE=/opt/devkitpro/cmake/WiiU.cmake -DCMAKE_BUILD_TYPE:STRING=RelWithDebInfo
cmake --build build-wiiu --target 2ship

# build wuhb
cmake --build build-wiiu --target 2ship_wuhb
```
