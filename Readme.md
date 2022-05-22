Robot image layer manifest
==========================

**DEPRECATED: You probably want [srobo/robot-image](https://github.com/srobo/robot-image).**

This repository contains the repo manifest for the layers used to build the robot images using yocto.

Quickstart
----------

To get going with the image you will need a computer with [repo][repo] and the [yocto dependancies][yocto-deps] installed.

Then run the following commands to setup the build environment (no need to checkout this manifest first).

```
mkdir srobo-build
cd srobo-build
repo init -u git@github.com:srobo/robot-image-manifest
repo sync
```

You can then activate the build environment in a terminal by running the following, it is best to run this in bash as some shells dont work correctly with yocto.

```
source ./setup-odroid-build
```

The image can then be built by running the following command, this will take some time on the first build as it downloads and build all components of the image.

```
bitbake srobo-image-robot
```

[repo]: https://source.android.com/setup/develop#installing-repo
[yocto-deps]: https://www.yoctoproject.org/docs/2.4.2/yocto-project-qs/yocto-project-qs.html#packages
