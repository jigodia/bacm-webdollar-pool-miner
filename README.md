# BACM miner installation steps !

- sudo -i
- sudo su
- bash <(curl -s https://raw.githubusercontent.com/jigodia/install/master/miner.sh)   
- cd bacm-miner
- nano wallet.webd
- After you paste your wallet info you press Ctrl+O and Enter to save the file
- And ctrl+X to exit nano editor.
- chmod +x wallet.webd                                                
- npm run commands  
- Select 4 from the menu list and then type wallet.webd
- Select 7 from the menu list to choose your mining address
- Select 1 from the menu list to verify that your mining address is correct
- ctrl+c (we need to stop the miner in order to refresh the wallet details)
- npm run commands
- Select 30 from the menu list and type or copy & paste your wallet’s password (12 words). It’s the seed word where you encrypted your wallet.
- Select 10 from the menu list to mine in the BACMpool.

# If npm will not be install use this :

# install nvm
wget -qO- \
    https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash

# export nvm required env
export NVM_DIR="${HOME}/.nvm"
# this loads nvm
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"

# install node long term version
nvm install --lts

# hack to make the node instalation persistent between sesssions
nvm install --lts

# install node 8 version.

nvm deactivate && nvm uninstall v10.15.3

cd ~
curl -sL https://deb.nodesource.com/setup_8.x -o nodesource_setup.sh

sudo bash nodesource_setup.sh

sudo apt-get install -y nodejs

cd bacm-miner && rm -fr node_modules && npm install 


