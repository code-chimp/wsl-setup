# Hyperledger Tooling

``` bash
# composer tools will not work with node higher than 8.x
nvm install v8.15
nvm use lts/carbon
npm i -g composer-cli composer-rest-server composer-playground yo generator-hyperledger-composer

# create a directory for the tools
mkdir /c/work/hyperledger
cd /c/work/hyperledger

# running the via curl doesn't seem to work as advertised
# pulling it local seems to get around the issue
wget -O bootstrap.sh http://bit.ly/2ysOFE
chmod +x bootstrap.sh
# gets the samples and downloads docker images
./bootstrap.sh
# gets the binary tools
./bootstrap.sh -d -s
```

## Add to your `.bashrc`
```bash
export HLF=/c/hyperledger
export PATH=$HLF/bin:$PATH
```

## Chaincode w/ Golang

``` bash
# if you don't already have this installed
sudo apt install golang-go

# make sure you have $GOPATH/bin on your PATH
mkdir -p  $GOPATH/src/github.com/hyperledger
cd $GOPATH/src/github.com/hyperledger
git clone https://github.com/hyperledger/fabric
git clone https://github.com/hyperledger/fabric-ca
cd fabric
make docker
make configtxgen cryptogen
cd ../fabric-ca
make docker
```
