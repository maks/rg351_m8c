# m8 Headless for RG351 devices

This setup should work for a variety of rg351 devices, including the rg351m, rg351mp, and rg351v. It requires a custom firmware install. Instructions will focus on ArkOS but it may also work with 351Elec or TheRA with a few tweaks.

1. Install ArkOS following their directions. https://github.com/christianhaitian/arkos/wiki
2. Copy the M8 folder into /roms/ports/ directory (or /roms2/ports if you're using the second SD card on an rg351mp)
3. Put the SD card in your device and boot it up
4. Under Ports you should now see an m8 item with a few scripts
  - SETUP - will install libserialport and add your user to the proper group to interact with serial devices.
  - M8 - launches m8c
  - _setup_build_tools.sh - install headers and build tools for compiling m8c
  - _build_m8c.sh - build the binary
5. Run the SETUP task and then reboot the device to ensure the user group changes take effect
6. Now try running M8. If you're lucky it'll all work!

## Building

You can run the `_setup_build_tools.sh` and `_build_m8c.sh` scripts to rebuild m8c. Recommend running them in a terminal session so you can see the output.

## Problems

### No audio

Check alsamixer settings.
