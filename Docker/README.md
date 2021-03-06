# Docker {#docker}

[Docker](https://docs.docker.com/) is a platform for developers and sysadmins to develop, ship, and run applications. Docker lets you quickly assemble applications from components and eliminates the friction that can come when shipping code. Docker lets you get your code tested and deployed into production as fast as possible.

### Before you start {#before-you-start}

In order to simplify the installation process you should install homebrew-cask which provides a friendly homebrew-style CLI workflow for the administration of Mac applications distributed as binaries. Refer to [this](http://sourabhbajaj.com/mac-setup/Homebrew/Cask.html) article in order to install homebrew-cask.

### Install Stable {#install}

Use can use cask to install Docker Toolbox which is a collection of useful docker tools such as compose, machine and Kitematic.

```
$ brew cask install docker-toolbox
```

### Install Beta {#quick-start}

If you are looking for the cutting edge on Docker head over to the [Get Docker ](https://docs.docker.com/docker-for-mac/)page to download the latest stable version. 

### Quick Start {#quick-start}

For quick start find the Docker Quickstart Terminal and double click to launch it. Then you start the hello world container using:

```
$ docker run hello-world
```

You can find more about docker follow the [documentation here](https://docs.docker.com/).

