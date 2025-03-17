# The IdeaPad ACPI Extras kernel modules for ThinkBook 2024 G6+

This kernel module solves problem with laptop turning off after closing the lid.

Tested and works on:

- Thinkbook 2024 16+ IMH with Ubuntu 24.04 with kernel 6.9.3-060903-generic
- Thinkbook 16 G6+ 2024 AHP with Fedora 41 and kernel 6.13.7-cachyos

## Build

Clone the repo with amd-patch branch first:

```shell
git clone -b amd-patch https://github.com/MCPEngu/ideapad-laptop-tb2024g6plus 
```

Then:

```shell
cd ideapad-laptop-tb2024g6plus && make
```

## Usage

### Install via dkms

```shell
sudo make install-dkms
sudo reboot
```

### Uninstall via dkms

```shell
sudo make uninstall-dkms
sudo reboot
```


# Problem:
- Audio mute and mic LEDs not working. Waiting for this patch merge into stable: https://lore.kernel.org/lkml/20250222114532.4105-1-xy-jackie@139.com/
- Fn + F4 to mute mic not working.