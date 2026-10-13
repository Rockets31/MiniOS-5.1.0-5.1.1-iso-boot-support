# MiniOS-5.1.0/5.1.1-iso-boot-support
Directly boot & and install MiniOS 5.1.0 &amp; 5.1.1 from ISO image using grub2 without burning to usb-drive. (There is a bug in theses versions, so the builtin isoboot function is not working, so I provide an 'external' solution.)

# Features
- Filesystems: ext4, fat 
- Provide boot menu (basic)
- Supported ISOs: MiniOS 5.1.0 & 5.1.1 (standard, toolbox, ultra).

# Usage
Load provided 'MiniOS323.img' file along with the main 'initrd' of the installation media via grub loopback module.
If you are using 'https://github.com/Mexit/MultiOS-USB', it is just a few steps:

0. Use MultiOS-USB partition on 'ext4' or 'fat' filesystem.
1. Copy your MiniOS-iso files to 'ISOs' directory.
2. Create a directory for 'grub.cfg' files: '/MultiOS-USB/config_priv/minios-sc'
3. Copy 'minios510.img', 'minios-5.1.x-isoboot.cfg'  over there.
4. Reboot into 'MultiOS-USB' and start e.g. 'minios-trixie-xfce-ultra-amd64-5.1.1.iso [scandev]' entry.
5. MiniOS will start same way as from usb-stick.
