A best-of-both-worlds merge of [aria2c-daemon-arch](https://github.com/yhfudev/aria2c-daemon-arch) and [systemd-units](https://github.com/GutenYe/systemd-units)' [aria2 service](https://github.com/GutenYe/systemd-units/tree/master/aria2) to make an easy to install per-user aria2 service for arch linux.

## INSTALL

```
git clone https://github.com/Nimdraug/aria2c-daemon-arch.git
cd aria2c-daemon-arch
makepkg
pacman -U aria2c-user-daemon-0.1-1-any.pkg.tar.xz
```
