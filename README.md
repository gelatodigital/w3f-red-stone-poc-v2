
# Gelato Web3 functions <<-->> RedStone PoC

## Summary

Oracle that using RedStone and Gelato Web3 functions to:
- Push on-chain price if the price difference between stored and live price is gerater than 20%

## Demo
- Mumbai:
  - Smart Contract: [https://mumbai.polygonscan.com/address/0xb26a01df1913a9f1e9cdbaed240e8a38f724a673#readContract](https://mumbai.polygonscan.com/address/0xb26a01df1913a9f1e9cdbaed240e8a38f724a673#readContract)
  - Web3 Function: [https://beta.app.gelato.network/task/0xe5647565edb71d22583c74085b4dccd7e0c202569faa542caf99fd3d0d1d533d?chainId=80001](https://beta.app.gelato.network/task/0xe5647565edb71d22583c74085b4dccd7e0c202569faa542caf99fd3d0d1d533d?chainId=80001)

## Deploy your smart contract and web3 function
```
yarn run deploy 
```

## How to run

1. Install project dependencies:
```
yarn install
```

2. Create a `.env` file with your private config:
```
cp .env.example .env
```
You will need to input your `PROVIDER_URLS`, your RPC.


3. Test the  web3 function
```
npx w3f test web3-functions/redstone/index.ts --logs --chain-id=80001
```

4. Deploy the web3 function on IPFS
```
npx w3f deploy web3-functions/redstone/index.ts
```

 ✓ Web3Function deployed to ipfs.
 ✓ CID: QmWz7Y4fpoTxrXsHe1MK9qnk9bNUZrapMGGYiiEcm995JE

5. Create the task following the link provided when deploying the web3 to IPFS in our case:
```
https://beta.app.gelato.network/new-task?cid=QmWz7Y4fpoTxrXsHe1MK9qnk9bNUZrapMGGYiiEcm995JE
```
