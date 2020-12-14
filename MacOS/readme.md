# Use pre-compiled binary to run Paicoin on MacOS

Note: I have verified that these binary is runnable in MacOS Catalina and Big Sur.

## 1. install brew and xcode
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
and then install xcode from app store

## 2. install dependencies
```
brew install git miniupnpc libevent berkeley-db@4 boost
```
required minimum version:
miniupnpc@2.1    libevent@2.1.12    berkeley-db@4.8.30    boost@1.74

## 3. download pre-compiled binary
```
cd ~
git clone https://github.com/ybAmazing/paicoin_pre-compiled.git
```

## 4. execute paicoind
```
tar xzf ./paicoin_pre-compiled/MacOS/Catalina-paicoin.tar.gz
cd ./paicoin
./paicoind --daemon=1
```
it will cost some minutes to synchronize the blockchain.

## 5. check
```
./paicoin-cli getmininginfo
./paicoin-cli getstakeinfo
less ~/Library/Application\ Support/PAIcoin/debug.log
```
