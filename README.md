Haskell For Arch
================

My personal take on how Haskell packages should be built for [Arch Linux](https://www.archlinux.org/).

If you are adventurous you can add the following to your `/etc/pacman.conf` (place it second, just after `[core]`).

```
[mtrepo]
Server  = ftp://therning.org/$repo
```

The repo and packages are signed using my personal key `0x927912051716CE39`.
