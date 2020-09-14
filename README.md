# DFIPs
DeFiChain Improvement Proposals

Check [issues](https://github.com/DeFiCh/dfips/issues) for current proposals.

## Stages

Each accepted DFIPs would be going through 2 further stages: Request for Comment (RFC) and Voting.

### Request for Comment (RFC)

Each DFIPs will be presented as a GitHub Issue, allowing for free and open discussions among community members.

RFC period would typically last for 1 week.

### Voting

DeFiChain's consensus is to allow masternodes to make a vote on DFIPs. One masternode one vote.

As on-chain voting is not yet available, temporary voting procedure would be as follows:

1. A voting snapshot block would be announced.

2. Each masternodes will have at least 1 week to vote. Voting is currently carried out by signing a message from masternode owner signifying either a yes or no.

3. Submit the vote before the closing date or block via the same GitHub issue in the comment. 

4. If there are duplicate votes from the same notes, only the final posted votes count. Votes can be withdrawn by posting a neutral vote. Non-voting nodes are considered neutral.

### How to vote

1. Determine your decision and the string to sign. For example, for [DFIP #1](https://github.com/DeFiCh/dfips/issues/1), the decisions are either one of the following:

    - Yes, I agree. Sign: `dfip-1 yes`
    - No, I do not agree. Sign: `dfip-1 no`
    - Neutral. Sign: `dfip-1 neutral`.

2. Get access to your owner's wallet, and sign either of the strings given. For instance if you agree, you would use the following command to sign:

    ```sh
    # OWNER_ADDRESS being your masternode's owner address
    defi-cli signmessage "dfip-1 yes" OWNER_ADDRESS 
    ```

3. At the closing date or block, a simple majority of the votes, excluding neutral votes, would determine the outcome of a decision.

