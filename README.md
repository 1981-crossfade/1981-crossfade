BTCPAYGEN_EXCLUDE_FRAGMENTS="$BTCPAYGEN_EXCLUDE_FRAGMENTS;opt-add-tor"
. btcpay-setup.sh -i
sudo su -
apt-get update && apt-get install -y git
if [ -d "bitcart-docker" ]; then echo "existing bitcart-docker folder found, pulling instead of cloning."; git pull; fi
if [ ! -d "bitcart-docker" ]; then echo "cloning bitcart-docker"; git clone sudo su - apt-get update && apt-get install -y git if [ -d "bitcart-docker" ]; then echo "existing bitcart-docker folder found, pulling instead of cloning."; git pull; fi if [ ! -d "bitcart-docker" ]; then echo "cloning bitcart-docker"; git clone https://github.com/bitcartcc/bitcart-docker bitcart-docker; fi export BITCART_HOST=bitcart.local export BITCART_CRYPTOS=btc,xmr export BITCART_ADDITIONAL_COMPONENTS=tor cd bitcart-docker ./setup.sh bitcart-docker; fi
export BITCARTGEN_DOCKER_IMAGE="bitcartcc/docker-compose-generator:local"
export BITCART_HOST=bitcart.local
export BITCART_CRYPTOS=btc
export BITCART_ADDITIONAL_COMPONENTS=tor
cd bitcart-docker
./setup.sh
