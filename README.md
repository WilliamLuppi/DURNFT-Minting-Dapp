# Welcome to William Luppi

![](https://github.com/WilliamLuppi/DURNFT-Minting-Dapp/blob/main/Logo.png)

All the code in these repos was created and explained by William Luppi on the main YouTube channel.

To find out more please visit:

[📺 YouTube](https://www.youtube.com/c/WilliamLuppi)

[🐶 Discord](https://discord.gg/Fe579jP8Pr)

[🐦 Twitter](https://twitter.com/williamlnfts)

[ℹ️ Website](https://dogsunleashednft.com)

# William Luppi NFT minting dapp 🔥

![](https://github.com/WilliamLuppi/DURNFT-Minting-Dapp/blob/main/Banner.png)

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/WilliamLuppi/DURNFT-Minting-Dapp.git
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `src` folder.

To link up your existing smart contract, go to the `src/contracts/contract.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "name": "Dogs Unleashed Roaming",
  "symbol": "DURNFT",
  "total_supply": 5000,
  "chain_symbol": "MATIC",
  "chain": "Polygon",
  "chain_id": 137,
  "address": "0x2862490C8CAf2aA3a259CdE41A17Cb679D6D1986",
```

Make sure you copy the contract ABI from remix and paste it in the `src/contracts/contract.json` file under the network and marketplace details.
(follow the youtube video if you struggle with this part).

Now you will need to create and change 1 image in the `src/assets` folder, `DURLogo.png`.

Next change the theme colors to your liking in the `src/styles/styles.css` file.

```css
:root {
  --button-bg: #8522c7;
  --button-active-bg: #681d9b;
  --small-button-bg: #919191;
  --small-button-active-bg: #646464;
  --large-button-bg: #ff0000;
  --button-text: #ffffff;
  --card: #ffffff;
  --accountText: #ffffff;
  --statusText: #470068;
  --bg-gradient_1: rgb(153, 61, 0);
  --bg-gradient_2: rgb(70, 26, 0);
  --gradient_1: rgb(255, 166, 0);
  --gradient_2: rgb(192, 189, 0);
  --gradient_3: rgb(255, 196, 0);
  --success: #24a13f;
  --warning: #ca5824;
  --error: #ca2f24;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Mint your Dogs Unleashed Roaming</title>
<meta name="description" content="Dogs Unleashed Roaming is an Collection of 5K Dogs on the Polygon Blockchain" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "Dogs Unleashed Roaming",
  "name": "Dogs Unleashed Roaming is an Collection of 5K Dogs on the Polygon Blockchain.",
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

If you have any problems pls feel free to ask for help in our <a href="https://discord.gg/Fe579jP8Pr">Discord</a>
