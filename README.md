# FHEM @ OpenWrt

## Description

Repository providing OpenWrt package feeds for FHEM.

```
# THIS IS A WORK IN PROGRESS
#
# PLEASE USE GITHUB ISSUES FOR ANY QUESTIONS
#
# https://github.com/fhem/openwrt/issues
```

## Feed for OpenWrt ≤ 24.10 (opkg based)

OpenWrt images up to ``24.10`` use [opkg](https://openwrt.org/docs/guide-user/additional-software/opkg) (a fork of ipkg) for package management. To install the FHEM repository on those versions, please follow these steps:

```
$ opkg install libustream-mbedtls
$ wget -P /tmp/ https://fhem.github.io/openwrt/fhem-public.key
$ opkg-key add /tmp/fhem-public.key

$ echo 'src/gz fhem https://fhem.github.io/openwrt/24.10/all' >> /etc/opkg/customfeeds.conf

$ opkg update
```


## Feed for OpenWrt ≥ 25.12 (apk based)

Starting with ``25.12``, and for current development snapshots, OpenWrt switched to [apk](https://openwrt.org/docs/guide-user/additional-software/apk) (Alpine Package Keeper) for package management. To install the FHEM repository, please follow these steps:

```
$ wget -P /etc/apk/keys/ https://fhem.github.io/openwrt/fhem-public-key.pem

$ echo 'https://fhem.github.io/openwrt/25.12/all/packages.adb' >> /etc/apk/repositories.d/customfeeds.list

$ apk update
```


## FHEM Installation

To setup a minimal FHEM with FHEMWEB, it is sufficient to request an installation of the FHEMWEB package: ``fhem-mod-fhemweb``

OpenWrt ≤ 24.10 (opkg):
```
$ opkg install fhem-mod-fhemweb
```

OpenWrt ≥ 25.12 (apk):
```
$ apk add fhem-mod-fhemweb
```

The package manager will automatically install the dependencies like ``perl``, misc. `perlbase` modules, ``fhem-bin`` and ``fhem-service``.

When using the LuCI web interface, you can search and install ``fhem-mod-fhemweb`` in _System/Software_, regardless of the package manager.


## Sources

The definitions (Makefiles) for these OpenWrt packages can be found [here](https://github.com/fhem/openwrt/tree/master/).
