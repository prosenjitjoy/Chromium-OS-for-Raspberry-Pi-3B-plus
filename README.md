# Chromium-OS-for-Raspberry-Pi-3B-plus
Original Repo - https://github.com/FydeOS/chromium_os-raspberry_pi

This repo contains all the modification needed on top of the original repo to successfully build chromiumos release 87 (32bit) for raspberry pi 3b+

To build it yourself, follow the [Chromium OS Developer Guide](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/developer_guide.md). The following steps apply only to build for chromium os release 87.

In 'Get the source code' section
```shell
cd ~/chromiumos
repo init -u https://chromium.googlesource.com/chromiumos/manifest -b release-R87-13505.B
repo sync -j4
```
After creating cros_sdk, exit from there and follow the instruction below.
```shell
mkdir ~/overlay
cd ~/overlay
git clone https://github.com/csjoy/Chromium-OS-for-Raspberry-Pi-3B-plus.git .
cp -r * ~/chromiumos/src/overlays
```
Then follow the rest of the guide using rpi3 as the board name.
```shell
(inside) export BOARD=rpi3
```

