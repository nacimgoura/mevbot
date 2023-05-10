# Mevbot V2 with Update mempool May 2023 (5 seconds faster than other bots)

1. Required to verify the contract on etherscan or bscscan. [READ THIS GUIDE](https://blog.chain.link/how-to-verify-a-smart-contract-on-etherscan/)
2. Minimum contract balance **0.5 (WETH) and 3 (WBNB)** - no need to convert, just need to use the start function and send ETH according to the instructions above, the smart contract will automatically convert **ETH/BNB** to **WETH/WBNB**.
3. ***IMPORTANT!*** Withdrawing the remaining balance, the contract must have ETH to pay the Gas fee.
4. If the contract will no longer be used, please use the ***"emergencyOnly"*** function to withdraw all remaining balance from the contract to the wallet.

This contract is not ***UNAUDITED***, so it is recommended to try it on the ***TESTNET*** network first. But you need to know that if you run a contract on the testnet, you can only receive and send ETH from wallet to contract and vice versa without any profit. 
Because the algorithm that the contract uses is only for Mainnet.
