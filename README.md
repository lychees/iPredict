# iPredict

Use Uniswap Single-Side Liquidity to create prediction markets with Market Protocol.

## Introduction

We propose a way to create a long-short token using Market Protocol and two conjugate uniswap pairs using a maker contract to manage the long-short token. Create prediction markets in such a way that the user experience is similar to that of uniswap, and users can make markets in them by providing single currency liquidity, earning commission income.

## Single-side Liquidity

You can add any ratio of tokens or ETH to a Uniswap pair.<br />
With this tool, for example, if there are 1 ETH + 400 DAI in a pair,<br />
you can add (1 ETH + 100 DAI) or (1 ETH + 0 DAI) or (0 ETH + 100 DAI) to the pool in one transaction.<br />
Behind the scenes, the contract swaps part of your token (or ETH) to the other token (or ETH) and then adds them all to the pair.<br />
The contract will find the best amount to swap to maximize the amount added into the pair with [this formula](https://www.wolframalpha.com/input/?i=solve+%28C+-+x%29+*+%28B+%2B+D%29+%3D+%28A+%2B+C%29+*+%28D+%2B+y%29%2C+%281000+*+A+%2B+997+*+x%29+*+%28B+-+y%29+%3D+1000+*+A+*+B).<br />

## Install Dependencies

`yarn`

## Compile Contracts

`yarn compile`

## Run Tests

`yarn test`
