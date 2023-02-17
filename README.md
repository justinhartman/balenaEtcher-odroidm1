# Balena Etcher Odroid M1 Ubuntu 22.04 Application

> A .deb package of the [balenaEtcher application](https://github.com/balena-io/etcher) for Odroid M1 running Ubuntu 22.04 (aarch64).

## Overview

There are a few repositories that have `arm` builds of Etcher but these did not work on the Hard Kernel Ubuntu 22.04 release for my Odroid M1. I built the source from scratch and have packaged it as a `.deb` file for all to use.

## Package Install

For your convienience, this package is published to [Packagecloud][packagecloud]. This means you can automate the install by downloading a `apt` repository and installing with `apt-get` or `apt`. 

### Add the APT Repository

To add the repo you can run the following script from a terminal console:

```sh
curl -s https://packagecloud.io/install/repositories/justinhartman/balenaEtcher-odroidm1/script.deb.sh | sudo bash
```

This will output the following:

```console
$ curl -s https://packagecloud.io/install/repositories/justinhartman/balenaEtcher-odroidm1/script.deb.sh | sudo bash
Detected operating system as Ubuntu/jammy.
Checking for curl...
Detected curl...
Checking for gpg...
Detected gpg...
Detected apt version as 2.4.8
Running apt-get update... done.
Installing apt-transport-https... done.
Installing /etc/apt/sources.list.d/justinhartman_balenaEtcher-odroidm1.list...done.
Importing packagecloud gpg key... Packagecloud gpg key imported to /etc/apt/keyrings/justinhartman_balenaEtcher-odroidm1-archive-keyring.gpg
done.
Running apt-get update... done.

The repository is setup! You can now install packages.
```

### Install Package

With the repo now added at `/etc/apt/sources.list.d/justinhartman_balenaEtcher-odroidm1.list` you can install the package as follows:

```sh
sudo apt install balena-etcher-electron
```

### Package Updates

Any future updates to the package will be included in any `apt upgrade` commands you run on the machine.

## Manual Install

If you'd rather just install the package feel free to download the latest file from Packagecloud or from the this repo using the instructions below.

1. Download the latest `.deb` file from [Packagecloud][packagecloud] or the [latest release page](https://github.com/justinhartman/balenaEtcher-odroidm1/releases/latest).
2. In terminal run the following command `sudo dpkg -i balena-etcher-electron_1.7.8+549d744d_arm64.deb` where you downloaded the file.

## Notes

- You may get an error about the package not installing; it has more than likely installed and can be run!
- It's an older version from 2022 because I had to use a branch that didn't rely on the chromium package which isn't supported on `arm`.
- I will try to make additional packages for newer versions.

[packagecloud]: https://packagecloud.io/justinhartman/balenaEtcher-odroidm1
