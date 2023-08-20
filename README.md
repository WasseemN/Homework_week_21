# Martian Token Crowdsale
<center><img src="Images/application-image.png"/></center>


## **Overview of the Token & Crowdsale Launch**
The Solidity smart contract is developed for the launch of KASEI coin, a fungible token based on the ERC-20 standard. A crowdsale contract is also deployed allowing buyers to participate in KASEI coin crowdsale. The process is executed on *Remix* IDE synced to the smart contract testing platform *Ganache* and hot storage wallets on *Metamask*.
****

## **Folder Structure**

* The `KaseiCoin.sol` contains the solidity smart contract code for the KaseiCoin contract.
* The `KaseiCoinCrowdsale.sol` contains the solidity smart contract code for the Crowdsale contract.
* The `Optional_KaseiCoinCrowdsale.sol` contains the solidity smart contract code for the Crowdsale contract of the optional challenge.
* The `Execution_Results` folder contains snapshots of the process execution of the smart contract on *Remix*.


## **Evaluation Evidence**

The process undertaken for the creation, deployment and crowdsale of the KASEI coin is provided in the figures below.

### Compiling Evidence

![KaseiCoin](Execution_Results/compile_KaseiCoin.png)

##### <center>Figure 1 - Compiling the KaseiCoin Contract


![KaseiCoinCrowdsale](Execution_Results/compile_KaseiCoinCrowdsale.png)

##### <center>Figure 2 - Compiling the Crowdsale Contract

![KaseiCoinCrowdsaleDeployer](Execution_Results/compile_KaseiCoinCrowdsaleDeployer.png)

##### <center>Figure 3 - Compiling the Crowdsale Deployer Contract


### Deploying and Testing the Smart Contract on Remix
The following presents the step-by-step execution of the smart contract on the *Remix* IDE as the testing platform. Once the contract is successfully compiled and deployed on the ethereum blockcahin, Ether deposits are made into the wallet for purchase of the KASEI coin and withdrawls are exhibited on the *Metamask* wallet.


![deploy_delpoyer](Execution_Results/deploy_deployer.png)

##### <center>Figure 4 - Deploy Deployer

![deploy_KASEICOIN](Execution_Results/deploy_KASEI_crowdsale.png)

##### <center>Figure 5 - Deploy Coin & Crowdsale

![Remix_Ganache](Execution_Results/connect_remix_ganache.png)



##### <center>Figure 6 - Link Remix & Ganache


![Metamask_Link](Execution_Results/connect_metamask.png)


##### <center>Figure 7 - Link Metamask


![Buyer](Execution_Results/buyer_wallet.PNG)

##### <center>Figure 8 - Create Buyer Wallet


![pruchase_KASEI](Execution_Results/purchase_KASEI.PNG)



##### <center>Figure 9 - Purchase KASEI


![transaction](Execution_Results/transaction_success.PNG)


##### <center>Figure 10 - Transaction Sucecss


![received_KASEI](Execution_Results/KASEI_recieved.PNG)

##### <center>Figure 11 - KASEI Receieved

## **Optional: Extend the Crowdsale Contract by Using OpenZeppelin**

This section illustrates the sucessfull completion of the optional challenge. Additional OpenZeppelin contracts have been inherited to the existing contract allowind additional functionality to the crowdsale - `CappedCrowdsale` to set a cap for the goal of ETH to be raised, `TimeCrowdsale` to set a time limit for when the crowdsale opens and closes and `RefundablePostDeliveryCrowdsale ` to refund investors if goal is not reached.

### Compiling Evidence

![KaseiCoinCrowdsaleDeployer2](Execution_Results/Optional_challenge/compile.PNG)

##### <center>Figure 12 - Compiling the Updated Crowdsale Deployer Contract


### Deploying and Testing the Updated Smart Contract on Remix
The following section presents the step-by-step execution of the updated smart contract on the *Remix* IDE as the testing platform. The functionality of the updated contract is tested to raise funds within the allowed time frame (for convenience the crowdsale is set to close within 2 minutes). The goal (30ETH) was reached within the timeframe and evidence below shows the crowdsale could not be finalized (and ETH successfully collected) until the close time was reached. 
<br>

<sup>
Note: A function to display the real-time Unix was necessary to be added to the deployer contract in order for these additional features to function properly. Otherwise the status of *isOpen()* remains unchanged indefinitely.</sup>
<br>



![deploy_delpoyer2](Execution_Results/Optional_challenge/deploy_deployer.PNG)

##### <center>Figure 13 - Deploy New Deployer

![goal_reached](Execution_Results/Optional_challenge/goal_reached_before_close.PNG)

##### <center>Figure 14 - Goal Reached Before Close Time

![finalize_attempt](Execution_Results/Optional_challenge/finalize_fail_before_close.PNG)

##### <center>Figure 15 - Finalize Attempt Before Close


![time_closed](Execution_Results/Optional_challenge/closed_before_finalize.PNG)

##### <center>Figure 16 - Crowdsale Closed

![finalize_success](Execution_Results/Optional_challenge/finalize_successful_ETH_transferred.PNG)

##### <center>Figure 17 - Crowdsale Finalized & ETH Transferred
