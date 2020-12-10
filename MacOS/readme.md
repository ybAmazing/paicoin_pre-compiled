# Use pre-compiled binary to run Paicoind on MacOS

## 1. install brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 2. install dependencies
```
brew install berkeley-db@4 boost
```

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

## 5. check
```
less ~/Library/Application\ Support/PAIcoin/debug.log
```
