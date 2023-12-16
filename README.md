# Simple X Locker

`slock` is the simple screen locker utility for X.

## Upstream

The upstream development for `slock` can be found [here](https://git.suckless.org/slock).

# Patches

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
git clone https://github.com/hooregi/slock.git
cd slock
sudo make clean install
```
