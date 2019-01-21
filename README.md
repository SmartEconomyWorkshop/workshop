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
sudo docker run -it --name neo-console-userX -v ~/smarteconomy/data:/app/data --restart=unless-stopped smarteconomyworkshop/neo-python:userX
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

# To connect to the neo-python prompt:
neo-console

# To open a shell in the container:
neo-console-shell
```

You can always detach from a Docker container with `Ctrl-P-Q`

## Bootstrap

If you want to bootstrap the blocks directly to disk, to save some time on syncing, you can download [the workshop bootstrap file](https://static.smarteconomyworkshop.org/bootstrap.tar.gz) and extract it in your `Chains` directory. This should create the `Workshop` and `Workshop_Notif` directories with the blocks. Please make sure to first stop your `neo-python` instance and clear the contents of the `Chains` directory.

# Interacting with your wallet

Once you have your NEO python console open, you can start interacting with your wallet and the blockchain. With the built-in neo-python compiler you can easily compile smart contracts to test them and deploy them. We have already loaded your wallets with some funds so you can get going easily.

  First open and take a look at your personal wallet, the password is `smarteconomy`

```
# Open your wallet
wallet open wallet.json

# Use the password: smarteconomy

# Now check your wallet
wallet

# We can now add the script hash for the Workshop Euro token:
wallet import token 0x468d4742becd5512a729aa1565b44589fc31f873
```

If your wallet is not fully synced, your balances will not show up. Make sure that `percent_synced` is at 100% before you continue. If at any time you feel like something is not quite okay with your wallet or balances, you can use `wallet rebuild` to start syncing from scratch. This should take a couple of minutes.

  In the `wallet` overview you can check your address and your address script hash, that should look like this:

```
Script hash b'\xadU\xc1QmV\x19;\x17\x7flq\xc7\x97\xeb\x18J\xba\x16\xe2' <class 'bytes'>
```

## Spend tokens or assets

Send some love, buy a virtual cup of coffee. Ask your neighbour for his NEO address and send him a couple of euro's:

```
wallet send EUR AMd14Q5C6YYGrz1cQA7GjfhgaNagrUkYzP 5 --from-addr=AH5HhymNXdQ14W4CbFjoqmkRPAcrjpSZRT
```

Now both check your wallet and notice that the tokens have moved:
```
wallet
```

# Challenges

Please make sure to check out our [neo-boa code examples and documentation](examples/README.md) first.

  When you are ready, go to [the challenges page](challenge/README.md) to pick your challange for today.

**Good Luck!**
