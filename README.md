<p align="center">
  <img src="https://neo-cdn.azureedge.net/images/neo-logo/144.png" width="144px;" alt="NEO">
</p>

<h3 align="center">NEO Smart Economy Workshop</h3>

# Introduction

Welcome to the NEO Smart Economy workshop on Monday 21 January in Geneva. During the workshop, please join us on our Flock chat channel, so we can communicate with each other and share questions and information.

[![Flock](http://static.flock.co/flock/images/flocklogo.png)](https://smarteconomy.flock.com/)

You can enter your e-mail address and join.

# Preparing your environment

Everybody will get a unique user id to be used during the workshop. For all tasks, please use only this unique number. When we mention `userX` in this documentation, then you should replace `X` with your unique number.

## Preferred

We prefer that you install the requirements on your own workstation. Install Git and Docker on your workstation, start pulling the image and clone the workshop repository. Now you can connect to our dedicated private net and start using the NEO blockchain.

### If you are on Linux:

```bash
# Install packages
sudo apt install git docker.io

# Create a working directory and pull the Git repository
mkdir ~/smarteconomy
cd ~/smarteconomy
git clone https://github.com/SmartEconomyWorkshop/workshop.git

# Pull the Docker image and create a local container
mkdir ~/smarteconomy/data
docker run -it --name neo-console-userX -v ~/smarteconomy/data:/app/data --restart=unless-stopped smarteconomyworkshop/neo-python:userX
```

### On Mac or Windows

* [Installation instructions by Atlassian on how to install Git on Mac OS X](https://www.atlassian.com/git/tutorials/install-git#mac-os-x)
* [Installation instructions by Atlassian on how to install Git on Windows](https://www.atlassian.com/git/tutorials/install-git#windows)
* [Install Docker Desktop for Mac instructions by Docker.io](https://docs.docker.com/docker-for-mac/install/)
* [Install Docker Desktop for Windows instructions by Docker.io](https://docs.docker.com/docker-for-windows/install/)

Once installed, please pull the image and run the container.

```bash
git clone https://github.com/SmartEconomyWorkshop/workshop.git
docker run -it --name neo-console-userX -v ~/smarteconomy/data:/app/data --restart=unless-stopped smarteconomyworkshop/neo-python:userX
```

## Alternative

If you are unable to use Docker on your workstation, you can get SSH access to our server and use Docker there. Please ask us for credentials and you can login using a shell terminal, like PuTTY on Windows.

```bash
ssh userX@smarteconomyworkshop.org
neo-console
```

# Interacting with your wallet

# Challenges

