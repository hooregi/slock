# Simple X Locker

`slock` is the simplest X screen locker. It is stable and quite a lot of people in the suckless community are using it every day when they are out with friends or fetching some food from the local pub.

## Upstream

The upstream development for `slock` can be found [here](https://git.suckless.org/slock).

# Patches

- [media](https://tools.suckless.org/slock/patches/mediakeys/)
- [xresources](https://tools.suckless.org/slock/patches/xresources/)

# Arch Linux Install

Download the`PKGBUILD` from this repository and run the following command:

```
makepkg -cf
```

This will create a file that ends in `.pkg.tar.zst`. Then run:

```
sudo pacman -U *.pkg.tar.zst
```

# Regular Install

Download the source code from this repository:

```
git clone https://gitlab.com/Hooregi/slock.git
cd slock
sudo make clean install
```
