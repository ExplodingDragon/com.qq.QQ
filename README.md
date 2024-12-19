# QQ

Tencent QQ (Chinese: 腾讯QQ), also known as QQ, is an instant messaging software service and web portal developed by the Chinese technology company Tencent.


## Features

### Wayland

This package enables the flags to run on Wayland, however it is opt-in. To opt-in run:

```sh
flatpak override --user --socket=wayland com.qq.QQ
```

To opt-out do the same with `--nosocket=wayland`.


## Legality

The QQ app itself is **proprietary** (closed source).

This wrapper is not verified by, affiliated with, or supported by Tencent.


## Install && Run

```bash
git clone https://github.com/ExplodingDragon/com.qq.QQ
cd com.qq.QQ 
sudo apt install flatpak flatpak-builder appstream-compose -y
flatpak remote-modify flathub --user --url=https://dl.flathub.org/repo/
flatpak-builder --force-clean --user --install-deps-from=flathub --repo=repo  builddir com.qq.QQ.yaml
flatpak run com.qq.QQ
```