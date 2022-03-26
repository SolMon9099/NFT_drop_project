# buildspace Solana NFT Drop Project

## Prerequisite
1. [git Installation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. [node Installation](https://nodejs.org/en/download/)
3. [yarn Installation](https://classic.yarnpkg.com/lang/en/docs/install/)
4. [ts-node Installation](https://www.npmjs.com/package/ts-node#installation)

### metaplex install
```
git clone -b v1.1.1 https://github.com/metaplex-foundation/metaplex.git
```
yarn install --cwd ~/metaplex/js/
```
ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts --version
```

And then clone this repo
## create .env file in app folder with following

```
REACT_APP_CANDY_MACHINE_ID=`<Your Candy Machine Public Key>`
```
REACT_APP_SOLANA_NETWORK=devnet
```
REACT_APP_SOLANA_RPC_HOST=https://explorer-api.devnet.solana.com
```
## upload resources and init candy machine or update candy machine
```
ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts upload -e devnet -k ~/.config/solana/devnet.json -cp config.json ./assets
```
ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts verify_upload -e devnet -k ~/.config/solana/devnet.json
```
ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts update_candy_machine -e devnet -k ~/.config/solana/devnet.json -cp config.json
```
## run following commands

1. Run `npm install` at the root of your directory
2. Run `npm run start` to start the project