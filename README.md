# FHEM @ OpenWrt

## Purpose

This repository provides a set of makefiles, that are used by the OpenWrt build system, to

1. create binary feeds of .ipk or .apk packages, to facilitate the installation of FHEM on OpenWrt based routers and computers, and

2. create custom OpenWrt based firmware images, that include tailored FHEM installations

## Difference to preexisting solutions

Various howtos already exist, that describe the installation of full FHEM distributions on computers running OpenWrt, e.g.

- https://wiki.fhem.de/wiki/OpenWRT
- https://openwrt.org/docs/guide-user/services/automation/fhem

This project however strives to integrate FHEM seamless into OpenWrt, and allows a fine grained selection of FHEM modules to get installed, to save memory and allow an installation on lower end router devices and sbc's.

The FHEM distribution is broken down into many different packages and their dependencies, and the default configuration is crafted in a way that allows the software to run on read-only-devices, too.

The [README.md](fhem/README.md) file in the fhem/ subfolder provides some insight about the actual setup and workings.

## Installation

The instructions as well as the pre-compiled packages mentioned above can be found on [fhem.github.io/openwrt/](https://fhem.github.io/openwrt/).


## Typical use cases
_coming soon_

## Todos
_coming soon_
