Fuel Modular excution Ethereum Blockchain

Deploying a Contract on Fuel Network

Install Dependencies

sudo apt update
sudo apt upgrade -y
sudo apt-get install curl screen -y 

Install RUST

curl --proto '=https' --tlsv1.3 https://sh.rustup.rs -sSf | sh
source $HOME/.cargo/env
rustc --version
rustup install stable
rustup update stable
rustup default stable

Install GIT

sudo apt install git -y 

Install Fuel-Toolchain

curl https://install.fuel.network | sh

Setting FUELUP
fuelup toolchain install latest
fuelup self update
fuelup update && fuelup default latest

Creating Project
mkdir fuel-project && cd fuel-project
forc new counter-contract

Editing Contract
nano counter-contract/src/main.sw

Build Contract
cd counter-contract
forc build 

Deploying Contract
Importing wallet Phrase key from fuel wallet

forc wallet import
forc wallet account new

deploy contract
forc deploy --testnet
