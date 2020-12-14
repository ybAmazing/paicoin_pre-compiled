# Use pre-compiled binary to run Paicoin on Linux

Note: I have verified that these binary is runnable in CentOS-8.0-64bit, Ubuntu-18.04-64bit and Ubuntu-16.04-64bit.

## 1. install dependencies
if you are Ubuntu user, run the command :
```
sudo apt-get update -y
sudo apt-get install -y git libtool libevent-dev libssl-dev libzmq5-dev libboost-system-dev libboost-filesystem-dev \
                libboost-chrono-dev libboost-program-options-dev libboost-thread-dev libboost-test-dev libdb-dev libdb++-dev
```
if you are CentOS user, run the command :
```
sudo yum upgrade -y
sudo yum -y install epel-release
sudo yum install -y git libtool libevent-devel openssl-devel zeromq-devel boost-devel libdb-devel
```

## 3. download pre-compiled binary
```
cd ~/
git clone https://github.com/ybAmazing/paicoin_pre-compiled.git
```

## 4. execute paicoind
```
tar xzf ./paicoin_pre-compiled/Linux/Ubuntu-18.04-paicoin.tar.gz   # choose Ubuntu or CentOS up to your environment
cd ./paicoin
./paicoind --daemon=1
```
it will cost some minutes to synchronize the blockchain.

## 5. check
```
./paicoin-cli getmininginfo
./paicoin-cli getstakeinfo
less ~/.paicoin/debug.log
```
