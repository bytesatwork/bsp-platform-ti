# bytes at work AG BSP platform manifest

This contains the manifest for repo and is intended to simplify the build
procedure for bytePANEL by [bytes at work AG](https://www.bytesatwork.ch).

## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform.git -b thud
	repo sync

When this commands completed successful, the following command will setup a
Yocto Project environment for bytePANEL:

	MACHINE=bytepanel DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a development image:

	bitbake devbase-image-bytesatwork

The output is found in:

	tmp/deploy/images/bytepanel
