# ancient-ubuntu-docker
Docker base images of ancient Ubuntu versions.

[Github](https://github.com/iComputer7/ancient-ubuntu-docker) | [Docker Hub](https://hub.docker.com/r/icomputer7/ancient-ubuntu-docker/)

**NOTE: THESE VERSIONS OF UBUNTU HAVE BEEN DISCONTINUED BY CANONICAL AND NO LONGER RECIEVE UPDATES. I CAN NOT AND WILL NOT MAKE SECURITY UPDATES FOR THESE IMAGES. YOU HAVE BEEN WARNED.**

# Tags
* `latest` | Whatever has been pushed most recently. Don't use this tag in your Dockerfile because it will change to another version eventually.

* `karmic` | Ubuntu 9.10 "Karmic Koala" (Released Oct 29, 2009; EOL Apr 30, 2011)

* `lucid` | Ubuntu 10.04 LTS "Lucid Lynx" (Released Apr 29, 2010; EOL Apr 30, 2015)

* `gutsy` | Ubuntu 7.10 "Gutsy Gibbon" (Released Oct 18, 2007; EOL Apr 18, 2009)

* `jaunty` | Ubuntu 9.04 "Jaunty Jackalope" (Released Apr 23, 2009; EOL Oct 23, 2010)

* `intrepid` | Ubuntu 8.10 "Intrepid Ibex" (Released Oct 30, 2008; EOL Apr 30, 2010)

* `hardy` | Ubuntu 8.04 LTS "Hardy Heron" (Released Apr 24, 2008; EOL May 9, 2013)

* `dapper` | Ubuntu 6.06 LTS "Dapper Drake" (Released Jun 1, 2006; EOL Jun 1, 2011)

# Quickly start a container with a bash terminal

`docker run -it icomputer7/ancient-ubuntu-docker:(version) /bin/bash`

# Why? Why would you make this?
I did this just for fun. Maybe there's a legacy app that only works on old Ubuntu versions that needs to be containerized? Maybe you want to demonstrate that an old distro can use a modern kernel? Or show off your neofetch? I don't know.

# How did you do this?
I converted the already existing OpenVZ container templates into Docker.

# How can I build this myself?
Download `Dockerfile`, `sources.list`, and the `.tar.xz` file that all correlate to the version you want to build. Then open the folder in a terminal and run `docker build -t (name) .` to start the build process.

# How does this even work in the first place?
I have no idea but it does. Pretty neat, huh?

# Why do the repos show a 404 not found error?
That is because the apt repositories have been moved off of the main servers and onto `old-releases.ubuntu.com`. Try adjusting `/etc/apt/sources.list`

# Why isn't (package) included?
Add it yourself in your Dockerfile.
