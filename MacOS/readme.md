# install brew
> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# install dependencies
> brew install berkeley-db@4 boost

# untar pre-compiled binary
> tar xzf ./Catalina-paicoin.tar.gz

# execute paicoind
> cd ./Catalina-paicoin
> ./paicoind
