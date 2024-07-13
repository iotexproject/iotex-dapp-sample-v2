
# IoTeX dApp Sample V3

<a href="https://iotex.io/devdiscord" target="_blank">
  <img src="https://github.com/iotexproject/halogrants/blob/880eea4af074b082a75608c7376bd7a8eaa1ac21/img/btn-discord.svg" height="36px">
</a>

![8861650093939_ pic_hd](https://user-images.githubusercontent.com/448293/171796205-937711d1-e336-4770-9388-ec0b02de3b89.jpg)


This is a boilerplate template for making your awesome dApp on IoTeX and ETH, BSC, and other possible chains ([request here](https://github.com/iotexproject/iotex-dapp-sample-v2/issues/new))

Technology used in this template are

- [Next](https://github.com/vercel/next.js)
- [React](https://reactjs.org/)
- [TRPC](https://trpc.io/)
- [Typescript](https://www.typescriptlang.org/)
- [Mobx](https://mobx.js.org/README.html)
- [Matine](https://mantine.dev/core/theme-icon/)
- [Cypress](https://www.cypress.io/)

## Intro

A starter for React with Typescript with the fast Vite and the beautiful Matine, tested with the powerful Cypress.

## Cheat Sheet

Here's a cheat sheet list to help you get started quickly

```ts
import { rootStore, useStore } from '@/store/index';

const { god } = useStore();
// or const god = rootStore.god

god.isConnect;

god.currentChain;
god.currentChain.chainId; // for current connected chain id
god.currentChain.Coin; // eth/bnb/iotx
god.currentChain.Coin.balance; // current balance
// ... see ChainState

god.currentNetwork;
god.currentNetwork.account; // for current connected account address
// ... see NetworkState

god.setShowConnecter(); // to show/close the Wallet Selector

god.currentNetwork.loadBalance(); // to load chain coin balance

await rpc('query')({
  UniswapRouter: [
    { calls: [{ address: '0x95cB18889B968AbABb9104f30aF5b310bD007Fd8', chainId: 4689 }] },
    {
      swap: [
        {
          args: {
            sellToken: 'BUSD_b',
            buyToken: '0xb8744ae4032be5e5ef9fab94ee9c3bf38d5d2ae0',
            buyAmount,
            recipient: '0x2AcB8663B18d8c8180783C18b88D60b86de26dF2',
            offlinePrice: true
          }
        },
        {
          amount: true,
          data: true,
          router: true,
          path: {
            address: true,
            symbol: true,
            decimals: true,
            totalSupply: true
          }
        }
      ]
    }
  ]
});
```

## Generate sdk

```
$ npm i @smartgraph/cli -g
$ pnpm dev
$ smartgraph codegen -l http://localhost:3000/api/graphql -o ./src/lib

```

## Installation

Clone the repo and run `pnpm install`

## Start

After the successfull installation of the packages: `pnpm dev`

