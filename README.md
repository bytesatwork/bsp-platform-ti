# bytesatwork AG BSP platform manifest for AM62x and AM62lx based modules

This repository contains the manifest for [repo](https://source.android.com/setup/develop/repo) and is intended to
simplify the build procedure for byteDEVKIT AM62x and byteDEVKIT AM62lx by [bytesatwork AG](https://www.bytesatwork.io).

## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform-ti.git -b wrynose
	repo sync

When these commands are completed successfully, the following command will setup a
Yocto Project environment for:

### byteDEVKIT AM62x

	MACHINE=bytedevkit-am62x DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

	deploy-ti/images/bytedevkit-am62x

### byteDEVKIT AM62lx

	MACHINE=bytedevkit-am62lx DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

	deploy-ti/images/bytedevkit-am62lx


## Note
The software provided is optimized for development convenience and is not suitable for use in production.

## Support

Refer to our [byteWIKI](https://bytewiki.readthedocs.io/en/latest/softwaredevelopment.html) for comprehensive information and guidance on software development.

If you have any questions or encounter any issues while using our products or services, please don’t hesitate to reach out to our support team.

Please feel free to contact us at support@bytesatwork.ch for any questions, comments or pull requests.

We are here to help and will get back to you as soon as possible.
