# Pactus-install-node

System: Ubuntu 22.04

Server preparation

    sudo apt update && apt upgrade -y

    sudo apt install tmux git curl -y

    sudo apt install make clang pkg-config libssl-dev build-essential -y

Download the binary file 0.17.0

    curl --proto '=https' --tlsv1.2 -sSL  https://github.com/pactus-project/pactus/releases/download/v0.17.0/pactus_downloader.sh | sh && cd pactus-cli_0.17.0

Create a info:

    sudo ./pactus-daemon init -w ~/pactus --testnet

Run node

    tmux new -s pactus
    
--->>

    sudo ./pactus-daemon start -w ~/pactus

check: 

    cd node_pactus && ./pactus-daemon start -w ~/pactus

#Wallet

View your seed

    ./pactus-wallet --path ~/pactus/wallets/default_wallet seed

Check balance
Check balance Validator address or Reward address -> change your_address

    ./pactus-wallet --path ~/pactus/wallets/default_wallet address balance your_address

Stake

Stake to your Validator , please change your info

(reward address) 

(validator address) 

(amount to stake)

    ./pactus-wallet --path ~/pactus/wallets/default_wallet tx bond (reward address) (validator address) (amount to stake)

        
