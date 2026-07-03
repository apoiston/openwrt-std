# OpenWrt

---

### Basic Information

- **LAN Address**: [10.0.0.1](http://10.0.0.1/)
- **Target Platform**: `x86/64`
- **Firmware Version**: `OpenWrt SNAPSHOT`
- **Username**: `root`
- **Password**: `NONE`

### Firmware Download

- [Releases](https://github.com/apoiston/builder/releases)

### Package Download

- [extra](https://initextra.pages.dev/)

- [kmods](https://initkmods.pages.dev/)

- [packages](https://initpackages.pages.dev/)

### Common Commands

```shell
# update index
apk update
```

```shell
# install package
apk add -U luci-i18n-nikki-zh-cn luci-app-nikki nikki mihomo-alpha
```

```shell
# upgrade package
apk add -U -u mihomo-alpha nikki luci-app-nikki luci-i18n-nikki-zh-cn
```

```shell
# force reinstall package
apk add -U --force-reinstall mihomo-alpha nikki luci-app-nikki luci-i18n-nikki-zh-cn
```

```shell
# remove package and dependencies
apk del -r nikki
```

```shell
# kernel build information
cat /proc/version
```

```shell
# system information
ubus call system board
```

```shell
# flash firmware (save configuration over reflash)
sysupgrade /tmp/openwrt-x86-64-generic-erofs-combined-efi.img.gz
```

```shell
# flash firmware (do not save configuration over reflash)
sysupgrade -n /tmp/openwrt-x86-64-generic-erofs-combined-efi.img.gz
```

### Add Feed

```shell
# add key
wget -O /etc/apk/keys/initextra.pem https://initextra.pages.dev/public-key.pem
```

```shell
# add feed
echo https://initextra.pages.dev/snapshots/x86_64/extra/packages.adb >> /etc/apk/repositories.d/customfeeds.list
```

### Credits

- [Joseph Mory](https://github.com/nikkinikki-org/OpenWrt-nikki)

- [OpenWrt](https://github.com/openwrt/openwrt)

- [OpenWrt LuCI](https://github.com/openwrt/luci)

- [OpenWrt Packages](https://github.com/openwrt/packages)

- [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo)
