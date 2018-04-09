# linux_setup_tips
A list of tips and tricks to install linux on windows pc laptops

## No Trackpad
Try with a usb mouse plugged directly to the laptop

## Windows setup
- Disable Fast Boot
- Disable Hibernate
todo(dbosch) => Add tutorial links

## Bios Configuration
- Disable Secure Boot
- Enable CSM
todo(dbosch) => Add tutorial links

## Install with UEFI version

## Custom Partition
- Boot loader on main hard drive (same as Windows Boot partition). Be careful to launch UEFI Ubuntu (you can choose when you choose the USB partition to install the distro: `Ubuntu...` or `UEFI:Ubuntu`)
- Swap: 1x to 1.5x RAM size
- `/` root partition should be ext4

You can also have a separate `/home` partition to isolate data from the core OS. But it's a more advanced concept. Not useful/needed for students on day 1.


## Nvidia
> Highlight the Ubuntu entry in the GRUB boot menu and press the E key. Add nouveau.modeset=0 to the end of the linux line - press F10 to boot.

- `nouveau.modeset=0` prevent using the intel graphic card to use only the nvidia. Useful if laptop have both. Then you only use the nvidia one.
- Might need to install last drivers: `sudo apt-get install nvidia-current`
