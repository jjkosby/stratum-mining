Supports HybridScryptHash256 PoW for MediterraneanCoin (MED) - http://www.mediterraneancoin.org



#Description
Stratum-mining is a pooled mining protocol. It is a replacement for *getwork* based pooling servers by allowing clients to generate work. The stratum protocol is described [here](http://mining.bitcoin.cz/stratum-mining) in full detail.

This is a implementation of stratum-mining for scrypt based coins. It is compatible with *MPOS* as it complies with the standards of *pushpool*. The end goal is to build on these standards to come up with a more stable solution.

The goal is to make a reliable stratum mining server for scrypt based coins. Over time I will develop this to be more feature rich and very stable. If you would like to see a feature please file a feature request. 

**NOTE:** This fork is still in development. Many features may be broken. Please report any broken features or issues.

#Features

* Stratum Mining Pool 
* Solved Block Confirmation
* Job Based Vardiff support
* Solution Block Hash Support
* *NEW* HibridScryptSha256 Algorithm Support
* *NEW* SHA256 and Scrypt Algo Support 
* Log Rotation
* Initial low difficulty share confirmation
* Multiple *coind* wallets
* On the fly addition of new *coind* wallets
* MySQL/PostGres/SQLite database support
* Adjustable database commit parameters
* Bypass password check for workers
* Proof Of Work and Proof of Stake Coin Support
* Transaction Messaging Support


#Requirements
*stratum-mining* is built in python. I have been testing it with 2.7.3, but it should work with other versions. The requirements for running the software are below.
* Python 2.7+
* python-twisted
* stratum
* MySQL Server 
* Mediterraneancoin CoinDaemon

Other coins have been known to work with this implementation. 

#Installation

sudo apt-get install python-twisted python-mysqldb python-dev python-setuptools python-memcache python-simplejson
easy_install -U distribute
git clone https://github.com/jjkosby/stratum-mining.git
cd stratum-mining
git submodule init
git submodule update
cd externals/medcoin_hybrid
sudo python setup.py install
cd ~
cd stratum-mining/externals/stratum
sudo python setup.py install 

#Startup
=======
Start server:

cd

cd stratum-mining

twistd -ny launcher.tac





  


