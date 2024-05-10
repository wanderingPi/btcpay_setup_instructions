# Login into the server and create a folder for btcpay
```
# update the system first
sudo apt update

# make folder for btc pay
mkdir btcpayserver
cd btcpayserver

# clone the repository
git clone https://github.com/btcpayserver/btcpayserver-docker
cd btcpayserver-docker
```
# Setup all the enviroment variables
```
# Set the custom domain you chose to use
export BTCPAY_HOST="example.etcetera.com"

# Enable Monero support
export BTCPAYGEN_CRYPTO1="xmr"

# Enable automatic HTTPS reverse proxy + SSL certs via Nginx and LetsEncrypt
export BTCPAYGEN_REVERSEPROXY="nginx"

# Allows you to manage the BTCPay Server install from the web UI, update, etc.
export BTCPAY_ENABLE_SSH=true
```
# Install btcpay server
```
./btcpay-setup.sh -i
```
This will setup everything automatically,and at the end you will be able to create an account to manage the store

The first account you create on a server will automatically be the admin.
