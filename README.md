# Ethereum DApp for Tracking Items through Supply Chain

### Introduction

This project consists in a decentralized application (DApp) of a supply chain solution backed by the Ethereum platform. It has Solidity smart contracts that manage specific user permission controls as well as track and verify products authenticity. It demonstrates a commonly supply chain process between a buyer and a seller. The seller can add items to the inventory system stored in the blockchain and the buyer can purchase such items. the seller can mark an item as shipped and the buyer can mark an item as received as well.

The project has some UML diagrams (in the diagrams folder) as the activity diagram below to make it better to understand the flow of the product in the supply chain.

![activity](https://user-images.githubusercontent.com/29313947/128574567-22ad7f1c-c87c-4116-81ca-3787ae8ff59d.png)

**Important**: The project was made with the versions below, since Truffle v5 comes with Solidity v0.5 with many changes concerning mutability and visibility.

- Truffle v4.1.14 (core: 4.1.14)
- Solidity v0.4.24 (solc-js)
- Ganache CLI v6.12.2 (ganache-core: 2.13.2)

**Important**: The project didn't use any external **libraries** worth mentioning and also didn't use **IPFS** to host the frontend part decentralized as well.

### Getting Started

1. Clone this repository.
2. Install the dependencies with [NodeJS](https://nodejs.org/en/) and NPM.
3. Test the application making calls to the contract on the [Rinkeby Test Network](https://rinkeby.etherscan.io/).
4. Take a look at the transactions happening on the Rinkeby Test Network at [Etherscan](https://rinkeby.etherscan.io/) explorer.

### Dependencies

1. Create an [Ethereum](https://ethereum.org/en/) account. Ethereum is a decentralized platform that runs smart contracts.
2. Create an account and install the [Metamask](https://metamask.io/) extension on your web browser.
3. Create an [Infura](https://infura.io/) account to publish the contracts into the [Rinkeby Test Network](https://rinkeby.etherscan.io/).
4. Install [Truffle](https://www.trufflesuite.com/truffle) CLI. Truffle is the most popular development framework for Ethereum.
5. Use this passphrase with [Ganache](https://www.trufflesuite.com/ganache) command as a suggestion _"spirit supply whale amount human item harsh scare congress discover talent hamster"_. Ganache is part of the Truffle suite that you can use to run a personal Ethereum blockchain.

**Important**: You will need your personal passphrase from your Ethereum account to publish into the Rinkeby Test Network, hence the **.secret** file in the **truffle-config.js**, even tough being a test network.

### Instructions

1. Install the dependencies:

```powershell
  npm i
  npm i -g truffle@4.1.14
  npm i -g ganache-cli
```

2. Turn on the Ganache suite so that you will have pre-defined accounts to test the contracts:

```powershell
  ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

![image](https://user-images.githubusercontent.com/29313947/128574297-9b9d8102-fdc9-4378-953b-2109b9bcea14.png)

3. Migrate, compile and test the contracts with truffle (on a separate console). It will use the previously up and running ganache locally blockchain.

```powershell
  truffle migrate
  truffle compile
  truffle test
```

![image](https://user-images.githubusercontent.com/29313947/128574410-c52cf254-70b0-4d4e-b72e-6eae35799ba3.png)

4. Publish the contracts into the Rinkeby Test Network with your Infura key:

```powershell
  truffle migrate --reset --network rinkeby
```

5. Check out and test the DApp in the frontend with the command below. You can run on the ganache-cli window, since Ganache was only for testing purpose.

```powershell
  npm run dev
```

**Important**: As a reminder, the frontend of the application will interact with the contract on the [Rinkeby Test Network](https://rinkeby.etherscan.io/), not with the pre-built accounts and deployed contracts made by the Ganache suite, as you can see in the [browser's developer console](https://support.airtable.com/hc/en-us/articles/232313848-How-to-open-the-developer-console#:~:text=To%20open%20the%20developer%20console%20window%20on%20Chrome%2C%20use%20the,then%20select%20%22Developer%20Tools.%22).

### Output

Here is an example of the smart contract in the blockchain and the transactions on Rinkeby:

Etherscan info:

- Transaction ID: [**0x6b3dc37663772515e0464098be314717e109ccdfb882725ce65432161d8e4404**](https://rinkeby.etherscan.io/tx/0x6b3dc37663772515e0464098be314717e109ccdfb882725ce65432161d8e4404)
- Contract: [**0xcf5a7edb0a5967acab9b81eb06c021b81b9ce1af**](https://rinkeby.etherscan.io/address/0xcf5a7edb0a5967acab9b81eb06c021b81b9ce1af)

![image](https://user-images.githubusercontent.com/29313947/128574896-4a28763b-7e54-411b-9232-b8e94f376c6b.png)

![image](https://user-images.githubusercontent.com/29313947/128575122-f5f766b6-6e24-45df-a3f6-75a723eb8f3e.png)

![image](https://user-images.githubusercontent.com/29313947/128575646-5bd39fd8-14a2-4599-b643-85950b4334b7.png)
