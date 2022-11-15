# bytes at work AG BSP platform manifest for AM335x and AM62x based modules

This repository contains the manifest for [repo](https://source.android.com/setup/develop/repo) and is intended to
simplify the build procedure for byteDEVKIT AM335x and byteDEVKIT AM62x by [bytes at work AG](https://www.bytesatwork.io).

## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform-ti.git -b kirkstone
	repo sync

When these commands are completed successfully, the following command will setup a
Yocto Project environment for byteDEVKIT AM335x:

	MACHINE=bytedevkit-am335x DISTRO=poky-bytesatwork EULA=1 . setup-environment build

For byteDEVKIT AM62x use:

	MACHINE=bytedevkit-am62x DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

	tmp/deploy/images/bytedevkit-am335x

or:

	tmp/deploy/images/bytedevkit-am62x
