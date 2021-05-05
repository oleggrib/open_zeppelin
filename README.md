This project configured to use Truffle (not Hardhat). 
Also this project configured to use Alchemy (not Infura) to connect public blockchain. 


Rename secrets_example.json to secrets.json , open in the text editor and replace mnemonic (password for key) and ApiKeys with your values.
{
  "mnemonic": "back neck ...",
  "alchemyApiKeyRopsten": "ApV...",
  "alchemyApiKeyRinkeby": "lFZ..."
}

If you want to use truffle develop then you have to install "ganache-cli"

Create contract in the /contracts folder and run "truffle compile" to compile it

If you want to deploy contract then create deploy script in the /migrations folder and run command line command "truffle migrate --network rinkeby" , where "rinkeby" is network name from truffle-config.js