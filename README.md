1. Clone this repo
```
git clone https://github.com/PatrickAlphaC/web3_py_simple_storage
cd web3_py_simple_storage
```
2. Setup a [local ganache chain](https://www.trufflesuite.com/ganache)
3. Install requirements
```bash
pip install -r requirements.txt
```
4. Set your private keys and address, and adjust this section appropriately:
```python
# For connecting to ganache
w3 = Web3(Web3.HTTPProvider("http://0.0.0.0:8545"))
chaind_id = 1337
my_address = "0x94B806BB0e455576ea46193D9DBbB08d1cc57Da9"
private_key = os.getenv("PRIVATE_KEY")
```
To set your private key as an environment variable, run `export PRIVATE_KEY=0xasdfasdfasfdasf`. If you're confused on how environment variables work, just set:
```python
private_key = "0xYOUR_KEY_HERE"
```
5. Run 
```
python deploy.py
```

To run on a testnet, just change these variables to whatever testnet you want to work with:
```
w3 = Web3(Web3.HTTPProvider("http://0.0.0.0:8545"))
chaind_id = 1337
my_address = "0x94B806BB0e455576ea46193D9DBbB08d1cc57Da9"
private_key = os.getenv("PRIVATE_KEY")
```
And make sure you have testnet ETH for whatever testnet you're on!



Table of Contents
Resources For This Course
Questions
Windows Support
Lesson 0: Welcome To Blockchain
What is a Blockchain?
Making Your First Transaction
How Do Blockchains Work?
Consensus
The Future
Miscellaneous
Lesson 1: Welcome to Remix! Simple Storage
Everything in this section can be read about in the Solidity Documentation
Remix
Basic Solidity
Deploying to a "Live" network
Lesson 2: Storage Factory
Inheritance, Factory Pattern, and Interacting with External Contracts
Lesson 3: Fund Me
Payable, msg.sender, msg.value, Units of Measure
Chainlink Oracles
Importing from NPM and Advanced Solidity
Lesson 4: Web3.py Simple Storage
Installing VSCode, Python, and Web3
Our First Python Script with Web3.py - Deploying a Contract
Interacting with Our Contract in Python & Web3.py
Lesson 5: Brownie Simple Storage
Brownie Introduction
Installing Brownie
Brownie Simple Storage Project
Testing Basics
[Brownie console]
Lesson 6: Brownie Fund Me
Introduction
Dependencies, Deploying, and Networks
Funding and Withdrawing Python Scripts
Testing across networks
Git
Lesson 7: SmartContract Lottery
Introduction
Lottery.sol
Testing Lottery.sol
Lottery.sol Testnet Deployment
Lesson 8: Chainlink Mix
Brownie Mixes
Lesson 9: ERC20s, EIPs, and Token Standards
Lesson 10: Defi & Aave
Defi Intro
Aave UI
Programmatic Interactions with Aave
Testing
Lesson 11: NFTs
Non-Technical Explainer
Simple NFT
SimpleCollectible Testing
Advanced NFT
Advanced deploy_and_create
Creating Metadata & IPFS
Lesson 12: Upgrades
Introduction to upgrading smart contracts
Upgrades-mix and code
Testing Upgrades
Upgrades on a testnet
Bonus Lesson 13: Full Stack Defi
Defi Stake Yield Brownie Scripts & Tests
Testing our Defi Stake Yield Brownie Dapp
Front End / Full Stack
Closing and Summary
Security
Where do I go now?
Learning More
Community
Hackathons
Resources For This Course
Questions
Github Discussions
Ask questions and chat about the course here!
Stack Exchange Ethereum
Great place for asking technical questions about Ethereum
StackOverflow
Great place for asking technical questions overall
Windows Support
Setup your windows environment
Learn how to install all the tools you will need for this course on a windows machine
Lesson 0: Welcome To Blockchain
What is a Blockchain?
Bitcoin Whitepaper
Ethereum Whitepaper
Hybrid Smart Contracts
Blockchain Oracles
What is a blockchain
Making Your First Transaction
Metamask
Etherscan
Rinkeby Etherscan
Kovan Etherscan
Rinkeby Faucet (Check the link token contracts page)
NOTE: The Chainlink documentation always has the most up to date faucets on their link token contracts page. If the faucet above is broken, check the chainlink documentation for the most up to date faucet.
OR, use the Kovan ETH Faucet, just be sure to swap your metamask to kovan!
Gas and Gas Fees
Wei, Gwei, and Ether Converter
ETH Gas Station
How Do Blockchains Work?
Blockchain Demo
Public / Private Keys
Layer 2 and Rollups
Decentralized Blockchain Oracles
Block Rewards
Run Your Own Ethereum Node
Consensus
Consensus
Proof of Stake
Proof of Work
Nakamoto Consensus
The Future
Ethereum 2
Miscellaneous
DAOs




Lesson 1: Welcome to Remix! Simple Storage
💻 Code: https://github.com/PatrickAlphaC/simple_storage

Everything in this section can be read about in the Solidity Documentation
Remix
Basic Solidity
Versioning
Compiling
Contract Declaration
Types & Declaring Variables
uint256, int256, bool, string, address, bytes32
Default Initializations
Comments
Functions
Deploying a Contract
Calling a public state-changing Function
Visibility
Scope
View & Pure Functions
Structs
Intro to Storage
Arrays - Dynamic & Fixed sized
Compiler Errors and Warnings
Memory
Mappings
SPDX License
Recap
Deploying to a "Live" network
A testnet or mainnet
Find a faucet here
Connecting Metamask
Interacting with Deployed Contracts
The EVM


Lesson 2: Storage Factory
💻 Code: https://github.com/PatrickAlphaC/storage_factory

Inheritance, Factory Pattern, and Interacting with External Contracts
Factory Pattern
Imports
Deploy a Contract From a Contract
Interact With a Deployed Contract
Recap


Lesson 3: Fund Me
💻 Code: https://github.com/PatrickAlphaC/fund_me

Payable, msg.sender, msg.value, Units of Measure
Payable
Wei/Gwei/Eth Converter
msg.sender & msg.value
Chainlink Oracles
Decentralized Oracle Network Chainlink
Blockchains can't make API calls
Centralized Nodes are Points of Failure
data.chain.link
Getting External Data with Chainlink Oracles
Chainlink
Faucets and Contract Addresses
Kovan
Getting Price Information
Importing from NPM and Advanced Solidity
Decimals/Floating Point Numbers in Solidity
latestRoundData
Importing from NPM in Remix
Interfaces
Introduction to ABIs
Getting Price Feed Addresses
getPrice
Tuples
Unused Tuple Variables
Matching Units (WEI/GWEI/ETH)
getConversionRate
Matching Units (Continued)
SafeMath & Integer Overflow
using keyword
Libraries
SafeMath PSA
Setting a Threshold
Require
Revert
Withdraw Function
Transfer
Balance
this
Contract Owners
Constructor
==
Modifiers
Resetting
for loop
Array Length
Forcing a Transaction
Recap


Lesson 4: Web3.py Simple Storage
💻 Code: https://github.com/PatrickAlphaC/web3_py_simple_storage

Installing VSCode, Python, and Web3
Developer Bootcamp Setup Instructions (metamask, vscode, python, nodejs..)
VSCode
VSCode Crash Course
Extensions
Short Cuts:
VSCode Shortcuts
VSCode MacOS Shortcuts
Python
Install Troubleshooting
Terminal
Making a directory/Folder
Opening the folder up with VSCode
Creating a new file
Syntax Highlights
Remember to save!
Setting linting compile version
VSCode Solidity Settings
Formatting & Format on Save
Solidity Prettier
Python Black
pip
Our First Python Script with Web3.py - Deploying a Contract
Reading our solidity file
Running a Python Script in the Terminal
MaxOS Shortcuts
Windows Shortcuts
Linux Shortcuts
Compiling in Python
py-solc-x
compile_standard
Colorized Brackets
JSON ABI
Saving Compiled Code
Formatting JSON
Deploying in Python
Get Bytecode
Get ABI
Choose Blockchain to Deploy To
Local Ganache Chain
Ganache UI
Ganache Command Line
Web3.py
HTTP / RPC Provider
Private Keys MUST start with "0x"
Contract Object
Building a Transaction
Account Nonce
Calling "Constructor"
Transaction Parameters
Signing the Transaction
NEVER put your private key directly in your code
Setting Environment Variables (Windows, Linux, MacOS)
More on Windows Environment Variables
Exported Environment Variables Only Last the Duration of the Shell/Terminal
Private Key PSA
.env file
.gitignore
Loading .env File in Python
python-dotenv
Viewing our Transaction / Deployment in Ganache
Waiting for Block Confirmations
Interacting with Our Contract in Python & Web3.py
2 Things you always need
Contract Address
Contract ABI
Getting address from transaction receipt
Calling a view function with web3.py
Call vs Transact
Updating State with Web3.py
ganache-cli
Installing Ganache
Install Nodejs
Install Yarn
Working with ganache-cli
Open a new terminal in the same window
Deploying to a testnet
Infura
Alchemy
Using Infura RPC URL / HTTP Provider
Chain Ids
Wow this seems like a lot of work... Is there a better way?


Lesson 5: Brownie Simple Storage
💻 Code: https://github.com/PatrickAlphaC/brownie_simple_storage

Brownie Introduction
Some Users:
https://yearn.finance/
https://curve.fi/
https://badger.finance/
Installing Brownie
Installing Brownie
Install pipx
pipx install eth-brownie
Testing Successful Install
Brownie Simple Storage Project
A new Brownie project with brownie init
Project Basic Explanation
Adding SimpleStorage.sol to the contracts folder
Compiling with brownie compile
Brownie deploy script
def main is brownie's entry point
brownie defaults to a development ganache chain that it creates
Placing functions outside of the main function
brownie accounts
3 Ways to Add Accounts
accounts[0]: Brownie's "default" ganache accounts
Only works for local ganache
accounts.load("..."): Brownie's encrypted command line (MOST SECURE)
Run brownie accounts new <name> and enter your private key and a password
accounts.add(config["wallets"]["from_key"]): Storing Private Keys as an environment variable, and pulling from our brownie-config.yaml
You'll need to add dotenv: .env to your brownie-config.yaml and have a .env file
Importing a Contract
Contract.Deploy
View Function Call in Brownie
State-Changing Function Call in Brownie / Contract Interaction
transaction.wait(1)
Testing Basics
test_simple_storage.py
Arrange, Act, Assert
assert
brownie test
test_updating_storage
Pytest / Brownie Test Tips
Deploy to a Testnet
brownie networks list
Development vs Ethereum
Development is temporary
Ethereum networks persist
RPC URL / HTTP Provider in Brownie
The network flag
list index out of range
get_account()
networks.show_active()
build/deployments
Accessing previous deployments
Interacting with contracts deployed in our brownie project
[Brownie console]
brownie console

  
  Lesson 6: Brownie Fund Me
💻 Code: https://github.com/PatrickAlphaC/brownie_fund_me

Introduction
Setup
Dependencies, Deploying, and Networks
Dependencies
chainlink-brownie-contracts
remappings
Deploy Script (V1)
helpful_scripts.py
__init__.py
Deploy to Rinkeby
Contract Verification (publish_source)
The Manual Way
"Flattening"
The Programatic Way
Getting an Etherscan API Key
ETHERSCAN_TOKEN
Interacting with Etherscan
Deploying to Local Chains
Introduction to Mocking
Constructor Parameters
networks in our brownie-config.yaml
Copying Mock Contracts from chainlink-mix
Deploying and using our mock
Refactoring
Deploying to a persistent ganache
brownie attach
Adding a persistent brownie network
resetting a network build
Funding and Withdrawing Python Scripts
Whoops! Let's fix an issue...
Fund Script
Withdraw Script
Testing across networks
test_can_fund_and_withdraw
default networks
pytest pip install pytest
pytest.skip
brownie exceptions
mainnet-fork
Custom mainnet fork
Adding a development brownie network
brownie networks add development mainnet-fork-dev cmd=ganache-cli host=http://127.0.0.1 fork='https://infura.io/v3/$WEB3_INFURA_PROJECT_ID' accounts=10 mnemonic=brownie port=8545
Alchemy
brownie test --network mainnet-fork
brownie ganache vs local ganache vs mainnet-fork vs testnet...
Git
Installing Git
Creating a repository
First time with git
Adding our project to github
Tweet it out!

  
  Lesson 7: SmartContract Lottery
💻 Code: https://github.com/PatrickAlphaC/smartcontract-lottery

Introduction
Add a README.md
Defining the project
Is it decentralized?
Lottery.sol
basic setup
Main Functions
address payable[]
getEntranceFee & Setup
Chainlink Price Feed
brownie-config
SPDX
Matching Units of Measure
Can't just divide
Test early and often
Quick Math Sanity Check
deleting networks
Alchemy again
Enum
startLottery
Openzeppelin... Is this the first openzeppelin reference?
Openzeppelin Contracts Github
Randomness
Pseudorandomness
block keyword
block.difficulty
block.timestamp
keccack256
True Randomness with Chainlink VRF
Chainlink VRF Remix Version
Inheriting Constructors
Oracle Gas & Transaction Gas
Why didn't we pay gas on the price feeds?
Chainlink Node Fees
Request And Receive Introduction
Kovan Faucets
Funding Chainlink Contracts
Request And Receive Explanation
A Clarification
endLottery
returns (type variableName)
fulfillRandomness
override
Modulo Operation (Mod Operation %)
Paying the lottery winner
Resetting the lottery
Testing Lottery.sol
deploy_lottery.py
get_account() refactored
get_contract
contract_to_mock
Contract.from_abi
Adding the parameters to deploying to lottery
vrfCoordinatorMock and adding mocks
LinkToken and Mocks
Successful Ganache Deployment!
Python Lottery Scripts/Functions
start_lottery
Brownie tip: Remember to tx.wait(1) your last transaction
enter_lottery
end_lottery
Funding with LINK
brownie interfaces
Waiting for callback
Integration Tests & Unit Tests
Test all lines of code
test_get_entrance_fee
pytest.skip (again)
test_cant_enter_unless_started
test_can_start_and_enter_lottery
test_can_pick_winner_correctly
Events and Logs
callBackWithRandomness
Lottery.sol Testnet Deployment
topics
conftest.py

  
  Lesson 8: Chainlink Mix
💻 Code: https://github.com/smartcontractkit/chainlink-mix

Brownie Mixes

  
  Lesson 9: ERC20s, EIPs, and Token Standards
💻 Code: https://github.com/PatrickAlphaC/erc20-brownie-py

ERC20/EIP20 Standard
What is an ERC20?
Creating an ERC20
OpenZeppelin ERC20
Solidity 0.8
I Challenge you to code this yourself!
deploy_token.py
Copy paste helpful_scripts.py
Viewing our token in metamask
Adding to an exchange

  
  
  Lesson 10: Defi & Aave
💻 Code: https://github.com/PatrickAlphaC/aave_brownie_py_freecode

Defi Intro
Defipulse
Defillama
Aave Testnet Site
Paraswap
Decentralized Exchange
Aave UI
Kovan ETH
What is Aave?
Borrowing and Lending
Connecting to Aave
Depositing Tokens / Lending
Checking your transaction is correct
WETH Gateway
Interest Bearing Token (aToken)
Collateral
DAI
Stablecoin
Wrapped Bitcoin (wBTC)
Why borrow tokens?
Blockchain Fintech Tutorial
DISCLAIMER ABOUT BORROWING
Borrowing Tokens
Liquidations
Your health factor must be above 1
Solvent
Stable vs Variable Interest Rate
Repaying our borrows/loans
Reward token / governance token
Governance
Programmatic Interactions with Aave
Quant Defi Engineer
Aave Documentation
Setup
Converting ETH -> WETH
get_weth.py
IWETH
Kovan WETH Token Address: 0xd0a1e359811322d97991e03f863a0c30c2cf029c
Mainnet WETH Token Address: 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2
Converting WETH -> ETH with withdraw
aave_borrow.py
LendingPool
LendingPoolAddressProvider
LendingPool and LendingPoolAddressProvider Addresses
Fixing import dependencies
Aave Github
ERC20 Approve Function
IERC20 from Patrick's repo
deposit
getUserAccountData
Liquidation Threshold
Risk Parameters
Borrowing DAI
Getting DAI Conversion Rate
Chainlink Price Feeds
AggregatorV3Interface
borrow
Mainnet DAI Address: 0x6b175474e89094c44da98b954eedeac495271d0f
Aave Testnet Token Addresses
Repaying
Kovan Run
Viewing the transactions
Testing

  
  Lesson 11: NFTs
💻 Code: https://github.com/PatrickAlphaC/nft-demo

Non-Technical Explainer
End-to-end article
What is an NFT?
ERC721
Token URI
Token Metadata Example
IPFS
Simple NFT
brownie mix
Initial Setup
SimpleCollectible.sol
OpenZeppelin ERC721
Pug Image
NFT Constructor
NFT is a type of factory pattern
createCollectible
_safeMint
TokenURI & Metadata
Opensea listing example
Is this decentralized?
Ethereum Size and dStorage
Ethereum Size
dStorage Solutions
IPFS
You need to have your NFT attributes both on-chain and inside your tokenURI metadata
deploy_and_create.py
TokenURI used for the demo: https://ipfs.io/ipfs/Qmd9MCGtdVz2miNumBHDbvj8bigSgTwnr4SbyH6DNnpWdt?filename=0-PUG.json
IPFS Companion
Rinkeby Deployment
Opensea Example
SimpleCollectible Testing
What else with NFTs?
Advanced NFT
AdvancedCollectible.sol
Dungeons and Dragons Example
Double Inherited Constructors
createCollectible (Advanced)
tokenIdToBreed
Working with in-flight Chainlink VRF requests
Download the NFT images from the nft-mix
setTokenURI
_isApprovedOrOwner
Emit events when you update mappings
indexed event keyword
Advanced deploy_and_create
Move OPENSEA_URL to helpful_scripts
Deploying AdvancedCollectible
Opensea testnet is only compatible with Rinkeby
Rinkeby Chainlink VRF Contract Addresses
Speeding through adding functions from previous projects
Deploy to Rinkeby
create_collectible.py
A quick unit test
A quick integration test
Creating Metadata & IPFS
create_metadata.py
get_breed
Metadata Folder
metadata_template
NFT Metadata Attributes
Checking if Metadata file already exists
Uploading to IPFS
upload_to_ipfs
Download IPFS Command Line
Download IPFS Desktop
HTTP IPFS Docs
ipfs daemon
Pinata
Pinata Docs
Refactoring to not re-upload to IPFS
Setting the TokenURI
End-To-End Manual Testnet Test
Viewing on Opensea

  
  Lesson 12: Upgrades
💻 Code: https://github.com/PatrickAlphaC/upgrades-mix

Introduction to upgrading smart contracts
Original Video
Smart Contracts can be upgraded!
Does this mean they are not immutable?
Trail of Bits on Upgradeable Smart Contracts
The "Not Really Upgrading" / Parameterization Method
The Social Yeet / Migration Method
Contract Migration
Proxies
DelegateCall
Terminology:
Implementation Contract
Proxy Contract
User
Admin
Gotchas:
Storage Clashes
Function Selector
Function Selector Clashes
Proxy Patterns:
Transparent Proxy Pattern
Universal Upgrade Proxy Standard
Diamond/Multi-Facet Proxy
Upgrades-mix and code
Setup
Box.sol
BoxV2.sol
Getting the proxy contracts
Openzeppelin Proxy Github
01_deploy_box.py
Hooking up a proxy to our implementation contract
(Optional) Creating a Gnosis Safe
Initializers
Encoding Initializer Function
Assigning ABI to a proxy
Running the script
Upgrade Python Function
Testing Upgrades
Testing our proxy
Testing our upgrades
Upgrades on a testnet

  
  Bonus Lesson 13: Full Stack Defi
💻 Code: https://github.com/PatrickAlphaC/defi-stake-yield-brownie-freecode

FreeCodeCamp React
What are we building?
Setup
DappToken.sol
TokenFarm.sol
tokenIsAllowed
addAllowedTokens
mapping of a mapping
stakeTokens
issueTokens
getUserTotalValue
getUserSingleTokenValue
getTokenValue
setPriceFeedContract
unStakeTokens
Can this be reentrancy attacked?
Defi Stake Yield Brownie Scripts & Tests
deploy.py
Deploying DappToken
Deploying TokenFarm
Adding allowed tokens
ERC20 Kovan Faucet
If the link above does not work, you can get another ERC20 token using this faucet: Weenus ERC20 Faucet
Mocking our ERC20s
Testing our Defi Stake Yield Brownie Dapp
test_set_price_feed_contract
test_stake_tokens
Fixtures
test_issue_tokens
Now you try on tests!
Front End / Full Stack
Front End Introduction
Typescript
React
useDapp
npx
yarn
create-react-app
Layout
Testing Front End
yarn && yarn start
Connecting our wallets
Install useDapp
Header Component
Connect Button
Material-UI
Making our button nicer
Main.tsx
Sending brownie-config & build folder to our UI
Helper Config
TypeScript error suppression
Getting addresses
Ethers
Only support kovan
YourWallet
supportedTokens
State Hooks
Showing tokens
WalletBalance
ethersproject/units
BalanceMsg
Stake Form
Calling approve
useContractFunction
useEffect
Notifications
Make it pretty
Alerts
Shoutout to Matt for the help on the front end!

Closing and Summary
Security
Best Practices
Attacks
Oracle Attacks
Re-entrancy Attacks
Damn Vulnerable Defi
Ethernaut
Some Auditors
OpenZeppelin
SigmaPrime
Trail of Bits
Where do I go now?
Learning More
CryptoZombies
Dapp University
ChainShot
Ivan on Tech
Eat the Blocks
Patrick Collins
Austin Griffith
Nader Dabit
Ethereum.org
Community
Twitter
Brownie Discord
Ethereum Discord
Chainlink Discord
Reddit ethdev
Hackathons
CL Hackathon
ETH Global
ETH India
Be sure to check out project grant programs!

Vyper
From solidity course to vyper

And make today an amazing day!
