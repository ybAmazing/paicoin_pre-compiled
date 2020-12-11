# Use pre-compiled binary to run Paicoin on Linux

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
git clone https://github.com/ybAmazing/paicoin_pre-compiled.git
```

## 4. execute paicoind
```
cd ./paicoin_pre-compiled/Linux
tar xzf ./Ubuntu-18.04-paicoin.tar.gz   # choose Ubuntu or CentOS up to your environment
cd ./Ubuntu-18.04-paicoin
./paicoind --daemon=1
```
it will cost some minutes to synchronize the blockchain.

## 5. check
```
./paicoin-cli getmininginfo
./paicoin-cli getstakeinfo
less ~/.paicoin/debug.log
```
