# Swene V1

This repository contains the core smart contracts for the Swene V1 Protocol.

## Bug bounty

This repository is subject to a bug bounty program.

## Local Deployment

The smart contracts of Swene v1 can be deployed using a deploy script.

```js
async function main () {
  // We get the contract to deploy
  const Liquidity = await ethers.getContractFactory('LiquidityFarming');
  console.log('Deploying Liquidity...');
  const liquidity = await Liquidity.deploy();
  await liquidity.deployed();
  console.log('Liquidity deployed to:', liquidity.address);
}

main()
  .then(() => process.exit(0))
  .catch(error => {
    console.error(error);
    process.exit(1);
  });
```

## Licensing

The primary license for Uniswap V3 Core is the Business Source License 1.1 (`BUSL-1.1`), see [`LICENSE`](./LICENSE).
