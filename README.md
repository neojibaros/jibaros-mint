# Jibaros NFT Minting App

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/metaversedreams/jibaros-mint
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0x1b1F33A9eEf47565d195E1943845AaC1777312B8",
  "SCAN_LINK": "https://polygonscan.com/token/0x1b1F33A9eEf47565d195E1943845AaC1777312B8",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "Matic",
    "ID": 137
  },
  "NFT_NAME": "Jibaros",
  "SYMBOL": "JIBARO",
  "MAX_SUPPLY": 10000,
  "WEI_COST": 25000000000000000,
  "DISPLAY_COST": 0.025,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/jibaros",
  "SHOW_BACKGROUND": true,
  "WETH_ADDRESS": "0x7ceb23fd6bc0add59e62ac25578270cff1b9f619"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
