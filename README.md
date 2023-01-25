# DFIPs and CFPs 

This details how to participate in DFIPs and CFPs on DeFiChain. With the recent introduction of On-Chain Governance, it is important to follow all the steps outlined below to ensure your DFIPs/CFPs are submitted successfully on-chain. 


## Overview

There are 2 key phases to take note of for those who wish to submit a proposal:

1. Proposal submission: Every proposal has to be available on the blockchain for 130,000 blocks (approximately 45 days) before the vote becomes valid. This will be referred to as the proposal ingestion period.
2. Proposal voting period: Upon submission, all proposals are eligible for voting in the next 260,000 blocks (~90 days) . For proposals that have fulfilled the 130,000-block ingestion period, masternodes can vote for them across the next 45 days (130,000 blocks).


<img width="643" alt="Screenshot 2023-01-25 at 7 06 23 PM" src="https://user-images.githubusercontent.com/99634821/214547700-2e4b4b39-2fe4-45cc-a277-22d5ad6e09b6.png">

For more information, please see this blog [here](https://blog.defichain.com/dfip-cfp-schedule-changes/).


## Submit Proposals On-Chain

### Step 1: Submission of DFIPs and CFPs on Github / Reddit

   Submit your proposal on [Github](https://github.com/DeFiCh/dfips/issues) or via [Reddit](https://www.reddit.com/r/defiblockchain/). Engage the community and discuss with them on your proposal.

### Step 2: Generating command on DeFiScan

   Upon creating a submission on Github/Reddit, a command has to be generated for proposals to be submitted on-chain. 

1. To generate a command, head over to https://defiscan.live/, under the [‘On-Chain Governance'](https://defiscan.live/on-chain-governance) tab.
2. Select `Create proposal` .
3. Fill in the details. Once all details have been verified, a command line will be generated in the final step.
4. Copy the command line.



<img width="720" alt="Screenshot 2023-01-25 at 7 19 04 PM" src="https://user-images.githubusercontent.com/99634821/214550198-a228afa7-c72e-45ac-b3c4-757446c23ecc.png">
Image 1: Generate proposal command line by selecting ‘Create proposal’ on DeFiScan, under the On-Chain Governance tab 

<img width="588" alt="Screenshot 2023-01-25 at 7 20 10 PM" src="https://user-images.githubusercontent.com/99634821/214550387-9d725ab7-adce-4b15-b78e-2536ad30f8da.png">
Image 2: Fill up proposal submission details on DeFiScan


### Step 3: Submit command in full node wallet

This will be the final step to ensure your proposal is submitted on-chain, which then allows the community to start voting. 

1. Head over and sign in to your full-node wallet CLI.
2. Paste the command line generated on DeFiScan earlier.
3. Ensure that your wallet has sufficient funds for the proposal fee, as it will be deducted during this transaction.
Upon successful transaction, you should be able to view your proposal on DeFiScan, under the ‘On-Chain Governance’ tab. 

Alternatively, the community can also use community projects like the DeFiChain Light Wallet to create a DFIP/CFP proposal.

## Voting Proposals On-Chain

DeFiChain's consensus is to allow masternodes to make a vote on DFIPs. One masternode is eligible for one vote.

If there are duplicate votes from the same nodes, the final posted votes before the block end height for the proposal will be counted. Votes can be withdrawn by posting a neutral vote. Non-voting nodes are considered neutral votes.

At the end block height for each proposal, a simple majority of the votes, excluding neutral votes, would determine the outcome of a decision.


## How to vote on-chain

### Step 1: Generating voting command on DeFiScan

1. Under the `On-Chain Governance` tab on DeFiScan, select a proposal from the list that you want to vote on. This will bring you to the proposal details page. 
2. Within the details page, select ‘Submit proposal’. You will be prompted to key in your masternode ID, followed by your voting choice. 
3. Once all details have been verified, a voting command line will be generated in the final step. 
4. Copy the voting command line.

<img width="705" alt="Screenshot 2023-01-25 at 7 21 55 PM" src="https://user-images.githubusercontent.com/99634821/214550742-125d9870-8606-4200-ab8f-65f134a5bdf6.png">
Image 3: To generate a voting command line on-chain, select ‘Submit vote’ in the proposal details page located on the right


### Step 2: Submit voting command in full node wallet 

This will be the final step to ensure your vote is submitted on-chain. 

1. Head over and sign in to your full-node wallet CLI.
2. Paste the voting command line generated on DeFiScan.
3. Upon successful transaction, you should be able to view your vote under the proposal details page.
4. Repeat the process should you wish to vote on other open proposals. 


## Frequently Asked Questions (FAQs) 

### 1. How are proposal fees calculated?

For DFIPs:
    50 DFI for Vote of Confidence, or
    500 DFI for reallocation of block rewards.

For CFPs, it requires a fee of either 1% of the amount requested or 10 DFI, whichever is higher, for Community Fund Proposal.

### 2. Are there other ways to submit my proposals?

If you have downloaded DeFiChain mobile Light Wallet, you may also choose to submit your proposals on the app. You may find the submission button under the `Portfolio` tab.

### 3. Are there other ways to vote on open proposals? 

Voting is currently only available on the full node wallet. Do follow the instructions on how to vote on-chain. 

