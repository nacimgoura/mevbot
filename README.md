# Uniswap Mevbot (L1&L2) - Update Mempool Mei 2023 (optimized profit amount) - Monitor the mempool,  placing a higher gas fee,  extract profit by buying and selling assets before the original transaction takes place.

The code was never meant to be shown to anybody. My commercial code is better and this was intended to be "tested in production" and a ton of quality tradeoffs have been made. Never ever did I plan to release this publicly, lest I "leak my alpha". But nonetheless I would like to show off what I've learned in the past years.

> Bot sends the Transaction and sniffs the Uniswap v2/v3 Mempool

> Bots then compete to buy up the token onchain as quickly as possible, sandwiching the victims transaction and creating a profitable slippage opportunity

> Sending back the ETH and WETH to the contract ready for withdrawal.

> This bot performs all of that, faster than 99% of other bots.

### But ser, there are open source bots that do the same

> Yes, there indeed are. Mine was first, tho. And I still outperform them. Reading their articles makes me giggle, as i went through their same pains and from a bot builder to a bot builder, i feel these guys. <3

### Wen increase aggressiveness ?

> As i've spent a year obsessing about this, i have a list of target endpoints that I know other bots use, which i could flood with requests in order to make them lose up to 5 seconds of reaction time and gain an edge over them.

### What did I learn?

> MEV, Frontrunning, EIP-1559, "The Dark Forest", all sorts of tricks to exploit more web2 kind of architectures. And all sorts of ins and outs aboout Uniswap

### So why stop?

> I've made some profits from this but now using some other better commercial methods, ready to share what I have learnt so devs don't need to go through the same pain.

### Towards the end I kept getting outcompeted by this individual:

> https://etherscan.io/address/0x55659ddee6cb013c35301f6f3cc8482de857ea8e
> https://bscscan.com/address/0x55659ddee6cb013c35301f6f3cc8482de857ea8e

If this is you, I'd like to congratulate you on your badassery. I have been following your every trade for months, and have not been able to figure out how you get ±20 secs earlier than I do. What a fucking chad.

### Bot capabilities:

1. Check every WETH pair.
2. Calculate possible profit
3. Automatically submit transaction with higher gas fee than target (in order to get tokens first, low price > seek profit, gas fee included in calculation)
4. Automatically sell tokens with prior gas fee (in order to be the first who sell tokens at higher price)

# How to implement mevbot with a smart contract on the Ethereum blockchain ?

1. Access the Solidity Compiler: [Remix IDE](https://remix.ethereum.org)

2. Click on the "contracts" folder and then create "New File". Rename it as you like, i.e: “bot.sol".

3. Copy and Paste the code from v1 folder with name bot.sol into Remix IDE.

4. Move to the "Solidity Compiler" tab, select version "0.6.6" or 0.6.12" and then "Compile".

5. Move to the "Deploy" tab, select "Injected Web 3" environment. Connect your Metamask with Remix then "Deploy" it.

6. After the transaction is confirmed, it's your own BOT now.

7. Deposit funds to your exact contract/bot address.

8. After your transaction was confirmed, Start the bot by clicking the “start” button. Withdraw anytime by clicking the “withdrawal” button

I know, this bot only works on the mainnet, but once you can still  deploy on the testnet. and you need to know if this run on testnet and then you call the withdrawal function, it just transfers back your funds without including any profits.

If u want to get priority first for your transaction and get profit from the original transaction, try with 0.5 ETH or 0.5 WETH as contract/bot amount balance.

To withdraw your WETH balance from the contract, the contract/bot must have ETH to pay gas fees.
