# Balena Etcher Odroid M1 Ubuntu 22.04 Application

> A .deb package of the [balenaEtcher application](https://github.com/balena-io/etcher) for Odroid M1 running Ubuntu 22.04 (aarch64).

## Overview

There are a few repositories that have `arm` builds of Etcher but these did not work on the Hard Kernel Ubuntu 22.04 release for my Odroid M1. I built the source from scratch and have packaged it as a `.deb` file for all to use.

## Install

1. Download the [latest release](https://github.com/justinhartman/balenaEtcher-odroidm1/releases/latest) `.deb` file.
2. In terminal run the following command `sudo dpkg -i balena-etcher-electron_1.7.8+549d744d_arm64.deb` where you downloaded the file.

## Notes

- You may get an error about the package not installing; it has more than likely installed and can be run!
- It's an older version from 2022 because I had to use a branch that didn't rely on the chromium package which isn't supported on `arm`.
- I will try to make additional packages for newer versions.
