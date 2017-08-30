# cryptoautobuild
Automatically build cryptocoins

This is a very simple script to help automate the building of coins on your server. This has been built and tested on Ubuntu 16.04 only.

Usage is very simple, run the script and answer the following two questions;

1. Coin Name
2. Link to Coins github.

After that the build is fully automated. It will create a new folder called CoinBuilds if it doesnt already exist. Then it will clone the github in to that folder using the supplied coin name.

It then detects what commands to use to build the coin. 

This script WILL NOT install any dependicies needed to build. You must have that already setup on your server. Below is the configuration I am running and I have not had a coin fail yet unless there is a development issue with the coin itself.

Happy building!

As always Please Donate to BTC Donation: 1AxK9a7dgeHvf3VFuwZ2adGiQTX6S1nhrp

Compiling Linux Wallet on Ubuntu/Debian

Step 1. Install the dependencies.

sudo add-apt-repository ppa:bitcoin/bitcoin

sudo apt-get update

sudo apt-get install libdb4.8-dev libdb4.8++-dev build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git libboost-all-dev libminiupnpc-dev libqt5gui5 libqt5core5a libqt5webkit5-dev libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libqrencode-dev

Note: If you are on debian, you will also need to apt-get install libcanberra-gtk-module.

Step 2. 

curl -Lo builder.sh https://raw.githubusercontent.com/crombiecrunch/cryptoautobuild/master/builder.sh

bash builder.sh
