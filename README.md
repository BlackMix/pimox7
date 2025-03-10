Pimox - Proxmox V7 for the Raspberry Pi
===

Pimox is a port of Proxmox to the Raspberry Pi allowing you to build a Proxmox cluster of Rapberry Pi's or even a hybrid cluster of Pis and x86 hardware.

Requirements
---
* Raspberry Pi 4
* Pre-installed Debian __Bullseye__ based  ___64-bit___ OS (not 32bit)

Prechecks
---
1. In /etc/network/interfaces, give the Pi a static IP address. You cannot use dhcp.
2. In /etc/network/interfaces, remove any IPv6 addresses.
3. In /etc/hostname, make sure the Pi has a name.
4. In /etc/hosts, make sure this hostname corresponds to the static IP you previous set.

Install
---
1. Do this at the console, not over a network. The network will be reconfigured as part of the install.
2. sudo -s
3. curl https://raw.githubusercontent.com/pimox/pimox7/master/pimox.sh | sh

RPiOS64 autoinstall
---
0. Flash and startup the latest image from https://downloads.raspberrypi.org/raspios_arm64/ .
1. sudo -s
2. curl https://raw.githubusercontent.com/pimox/pimox7/master/RPiOS64autoinstall.sh > RPiOS64autoinstall.sh
3. nano RPiOS64autoinstall.sh
5. Adjust network and hostname settings.
6. chmod +x RPiOS64autoinstall.sh
7. ./RPiOS64autoinstall.sh
8. Type a new root password.
9. Retype new password.
10. Do __not__ touch it untill, reboot is done.

Notes
---
1. This repo just contains the precompiled debian packages. The original Proxmox sources can be found at https://git.proxmox.com
2. The (very minimally) patched sources to rebuild this can be found at https://github.com/pimox
