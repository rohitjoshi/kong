# Building Kong distributions

Kong can be distributed to different platforms like CentOS, Debian, Ubuntu and OS X. Here you find the scripts that will start the build process and output packages.

# Requirements

The build can only be started from OS X, and requires [Docker](https://www.docker.com/) to be available on the system.

# Build

```shell
$ /bin/bash build-package.sh [platform...]
```

- Building for every platform:

  ```shell
  $ /bin/bash build-package.sh all
  ```

- Building for specific platforms:

  ```shell
  $ /bin/bash build-package.sh osx centos:5 debian:8
  ```

Distributions will be placed under the `build-output` folder (should the folder not exist it will be automatically created).

**Warning:** This folder also contains a file called `build-package-script.sh` file. **Do not execute it**, it's used internally by the build.

## Supported Platforms

- `all`
- `centos:5`
- `centos:6`
- `centos:7`
- `debian:6`
- `debian:7`
- `debian:8`
- `ubuntu:12.04.5`
- `ubuntu:14.04.2`
- `ubuntu:15.04`
- `osx`