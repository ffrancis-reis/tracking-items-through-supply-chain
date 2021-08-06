# Ethereum DApp for Tracking Items through Supply Chain

### Introduction

This project consists in a decentralized application (DApp) of a supply chain solution backed by the [Ethereum](https://ethereum.org/en/) platform. It has smart contracts that manage specific user permission controls as well as track and verify products authenticity.

### Getting Started

1. Clone this repository.
2. Install the dependencies with [NodeJS](https://nodejs.org/en/) and NPM.
3. Test the application making calls to the contract on the [Rinkeby Test Network](https://rinkeby.etherscan.io/).
4. Take a look at the transactions happening on the Rinkeby Test Network at [Etherscan](https://rinkeby.etherscan.io/) explorer.

### Dependencies

1. Create an [Ethereum](https://ethereum.org/en/) account.
2. Create an account and install the [Metamask](https://metamask.io/) extension.
3. Create an [Infura](https://infura.io/) account to publish the contracts into the [Rinkeby Test Network](https://rinkeby.etherscan.io/).
4. Install [NodeJS](https://nodejs.org/en/) platform.
5. Install [Truffle](https://www.trufflesuite.com/truffle) CLI.
6. Use this passphrase with [Ganache](https://www.trufflesuite.com/ganache) command as a suggestion _"spirit supply whale amount human item harsh scare congress discover talent hamster"_.

**Important** You will need your personal passphrase from your [Ethereum](https://ethereum.org/en/) account to publish into the Rinkeby Test Network, hence the **.secret** file in the **truffle-config.js**, even tough being a test network.

### Instructions

1. Install the dependencies:

```powershell
  npm i
  npm i -g truffle@4.1.14
```

2. Turn on the Ganache suite so that you will have pre-defined accounts to test the contracts:

```powershell
  ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

3. Compile and test the contracts with truffle:

```powershell
  truffle compile
  truffle test
```

4. Publish the contracts into the Rinkeby Test Network with your Infura key:

```powershell
  truffle migrate --reset --network rinkeby
```

5. Check out and test the DApp in the frontend with the command below.

**Important** As a reminder, the frontend of the application will interact with the contract on the [Rinkeby Test Network](https://rinkeby.etherscan.io/), not with the pre-built accounts and deployed contracts made by the Ganache suite, as you can see in the [browser's developer console](https://support.airtable.com/hc/en-us/articles/232313848-How-to-open-the-developer-console#:~:text=To%20open%20the%20developer%20console%20window%20on%20Chrome%2C%20use%20the,then%20select%20%22Developer%20Tools.%22).

```powershell
  npm run dev
```

### Output

Here is an example of the interactions with the contract flowing in the chain and the transactions on Rinkeby:
