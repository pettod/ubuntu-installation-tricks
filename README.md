# Ubuntu Installation Tricks

[https://github.com/kfechter/LegionY530Ubuntu](https://github.com/kfechter/LegionY530Ubuntu)

[https://medium.com/@futakuchi0117/installing-ubuntu-18-04-on-lenovo-legion-y740-98cab6eb1c91](https://medium.com/@futakuchi0117/installing-ubuntu-18-04-on-lenovo-legion-y740-98cab6eb1c91)

[https://askubuntu.com/questions/1062633/how-to-make-nouveau-modeset-0-automatic-on-boot](https://askubuntu.com/questions/1062633/how-to-make-nouveau-modeset-0-automatic-on-boot)

[https://askubuntu.com/questions/19486/how-do-i-add-a-kernel-boot-parameter](https://askubuntu.com/questions/19486/how-do-i-add-a-kernel-boot-parameter)

## Lenovo Legion Y740 Ubuntu 20.04 Installation

1. Create bootable USB stick

1. Disable secure boot

1. Boot from USB stick

1. Press "e" key and add **nouveau.modeset=0** command line argument after "quiet splash" argument

1. Make this change permanent by adding it to `grub`. Run command: `sudo nano /etc/default/grub`

1. Add **nouveau.modeset=0** argument `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash nouveau.modeset=0"`

1. Update `grub`. Run command: `sudo update-grub`
