#Frontrunning Bot (Sandwich Bot) - EVM

## Overview

Logic inside a simple WETH <> TOKEN UniswapV2 sandwich bot

## Explainer

In every Uniswap V2 trade, the user (victim) will specify a minimum amount of output tokens they're willing to receive.

The job of the sandwich bot is to calculate how much of the output tokens they should buy (to push the price of the token up) to match the victim's minimum out requirement. This minimum out requirement on most cases will be 2%, but on extreme cases it can be as high as 20% on volatile pairs (such as the SHIBA-WETH pair during the craze).

Once the sandwich bot has calculated the optimal number of tokens to buy, it'll wait for the victim to buy their tokens, and immediately sell to gain a profit.

## Running the bot

Add your node and your private_key in the `.env` file. If you have your own sandwich bot contract, you can also change the `SANDWICH_CONTRACT` address.

How to get Private Key from Metamask: https://support.metamask.io/hc/en-us/articles/360015289632-How-to-export-an-account-s-private-key

```bash
yarn bot
```

And you should be good to go


## Tests

No tests. Test in prod. Something, something Zuck, move fast, break things, win ETH. 