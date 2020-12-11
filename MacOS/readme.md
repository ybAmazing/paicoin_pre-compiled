# Use pre-compiled binary to run Paicoin on MacOS

## 1. install brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 2. install dependencies
```
brew install git miniupnpc libevent berkeley-db@4 boost
```
required minimal version:
miniupnpc@2.1 libevent@2.1.12 berkeley-db@4.8.30 boost@1.72

## 3. download pre-compiled binary
```
git clone https://github.com/ybAmazing/paicoin_pre-compiled.git
```

## 4. execute paicoind
```
cd ./paicoin_pre-compiled/MacOS
tar xzf ./Catalina-paicoin.tar.gz
cd ./Catalina-paicoin
./paicoind --daemon=1
```
it will cost some minutes to synchronize the blockchain.

## 5. check
```
./paicoin-cli getmininginfo
./paicoin-cli getstakeinfo
less ~/Library/Application\ Support/PAIcoin/debug.log
```
