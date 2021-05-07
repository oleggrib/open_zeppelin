This project configured to use Truffle (not Hardhat). 
Also this project configured to use Alchemy (not Infura) to connect public blockchain. 


Rename secrets_example.json to secrets.json , open in the text editor and replace mnemonic (password for key) and ApiKeys with your values.
{
  "mnemonic": "back neck ...",
  "alchemyApiKeyRopsten": "ApV...",
  "alchemyApiKeyRinkeby": "lFZ..."
}

If you want to use truffle develop then you have to install "ganache-cli" and run it before fire commands like "truffle migrate --network development", because ganache starts "network development" 

Create contract in the /contracts folder and run "truffle compile" to compile it

If you want to deploy contract then create deploy script in the /migrations folder and run command line command "truffle migrate --network rinkeby" , where "rinkeby" is network name from truffle-config.js


If you need to use upgrades, then you MUST install truffle to the project(global install not enough), in other way you will get an error.

npm install --save-dev truffle
npm install --save-dev @openzeppelin/truffle-upgrades

use truffle migrate --network "networkName" to deploy contract and proxy with specified network 

truffle console --network "networkName" to interact with proxyContract


That article can also help you https://forum.openzeppelin.com/t/openzeppelin-upgrades-step-by-step-tutorial-for-truffle/3579