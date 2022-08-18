# KAI Coin crowdsale

The goal of this project is to deploy a **crowdsale** contract for a token. I imported contracts for Crowdsale, MintedCrowdsale, CappedCrowdsale, TimedCrowdsale and RefundablePostDeliveryCrowdsale from open zeppelin. The crowdsale is to be deployed with a rate of 1, where one token equal one Wei. The goal if to reaise **300 Ether**. For demonstration purposes the crowdsale is timed to now + 10 minutes, where now is the block time when the contract is deployed. 

### KaseiCoin ERC20 contract compiled ✅
I first deployed the `KaseiCoin.sol` contract which is the ERC20 token contract. Here is a successful compilation of the contract. 

![KaseiCoin ERC20 contract](./images/kai_coin.jpg)

### KaseiCoinCrowdsale Contract compiled ✅
I then compiled and successfully deployed my `KaseiCoincrowdsale.sol` smart contract. Heres is the confirmations.

![KaseiCoinCrowdsale Contract](./images/crowdsale_contract.jpg)


## CrowdsaleDeployer Contract deployed and walkthrough interaction (Video)

![Walkthrough Video](./images/kaiCoin_crowdsale.gif)

I was able to reaise **300 ETH** and can confirm that the crowdsale worked and was **finalized**. After finalization, the wallets that deposited ether can withdraw their tokens. There is possibilty to withraw your tokens before the crowdsale has been finalized.