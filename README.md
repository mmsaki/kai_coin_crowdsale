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

> Above here you will see walkthrough. Wait for about **30 seconds** as it takes time for it to load on github. 

I am able to deploy `KaseiCoinCrowdsaleDeployer` which after deploying I can call my `kasei_crowdsale_address` and `kasei_token_address`. I then selected my contracts and added the addresses to view and intereact with them in the editor configuration with the provided addresses. I confirm that `isOpen` is **true** and proceed to buy **50 Ether** with the first accoung as the beneficiary, then, another **250 Ether** with a second test account from my metamask. I check and confirm that `goalReached` is **true** and check `weiRaised`. You can alsoe confirm that the `closingTime` has reached in order to call `finalized` for the crowdsale. I made sure to import the **KAI** coin to my metamask to see the balance. After the crowsale is finalized I first call `withdrawTokens` and add the beneficiary address. This will withdraw that tokens to the address and also send the ether raised to the crowsale payable address. Checking metamask you can see that **250 KAI** wais deposited to the second account and **50 KAI** deposited in the first account. Going back to the `KaseiCoin` token address we can call `totalSupply` and we see `300000000000000000000` wei which is equivalent to `300` ether. 
 