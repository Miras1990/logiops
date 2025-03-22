# logiops

This is an unofficial driver for Logitech mice and keyboard.

This is currently only compatible with HID++ \>2.0 devices.

## Configuration
[Refer to the wiki for details.](https://github.com/PixlOne/logiops/wiki/Configuration)

You may also refer to [logid.cfg](./logid.cfg) for an example.

Default location for the configuration file is /etc/logid.cfg, but another can be specified using the `-c` flag.

## Dependencies

This project requires a C++14 compiler, `cmake`, `libevdev`, `libudev`, and `libconfig`. For popular distributions, I've included commands below.

**Arch Linux:** `sudo pacman -S cmake libevdev libconfig pkgconf`

**Debian/Ubuntu:** `sudo apt install cmake libevdev-dev libudev-dev libconfig++-dev`

**Fedora:** `sudo dnf install cmake libevdev-devel systemd-devel libconfig-devel gcc-c++`

**Gentoo Linux:** `sudo emerge dev-libs/libconfig dev-libs/libevdev dev-util/cmake virtual/libudev`

**Solus:** `sudo eopkg install libevdev-devel libconfig-devel libgudev-devel`

**openSUSE:** `sudo zypper install cmake libevdev-devel systemd-devel libconfig-devel gcc-c++ libconfig++-devel libudev-devel`

## Building

To build this project, run:

```bash
mkdir build
cd build
cmake ..
make
```

To install, run `sudo make install` after building. You can set the daemon to start at boot by running `sudo systemctl enable logid` or `sudo systemctl enable --now logid` if you want to enable and start the daemon.

## Compatible Devices

[For a list of tested devices, check TESTED.md](TESTED.md)
