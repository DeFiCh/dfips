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

As on-chain voting is not yet available, voting will be conducted using message signing and verification process as follows:

1. A voting snapshot block would be announced at respective DFIP issues.

2. Each masternodes will have around 1 week to post a voting proof. Voting is carried out by signing a message from masternode owner with the desired decision.

3. Submit the vote before the closing date or block via the same GitHub issue in the comment. 

4. If there are duplicate votes from the same nodes, the final posted votes before the closing deadline count. Votes can be withdrawn by posting a neutral vote. Non-voting nodes are considered neutral.

## How to vote

1. Determine your decision and the string to sign. Please use the simple letters for the whole vote message(i.e. <proposal name>-<vote option>)  For example, for [DFIP #1](https://github.com/DeFiCh/dfips/issues/1), the decision options are:

    - Yes, I agree. Sign: `dfip-1-yes`
    - No, I do not agree. Sign: `dfip-1-no`
    - Neutral. Sign: `dfip-1-neutral`.

2. Get access to your owner's wallet, and sign either of the strings given. For instance if you agree, you would use the following command to sign:

    ```sh
    # OWNER_ADDRESS being your masternode's owner address with the collateral
    $ defi-cli signmessage OWNER_ADDRESS "dfip-1-yes"
    ```

3. Post your message and proof in the GitHub Issue as a message, using `8cmz6gLGJD7sTcjhkS6xG3CKkf68zKQHqF` as a sample owner's address. Ensure that the whole command and string is posted to allow independent verification.

    ```sh
    $ defi-cli signmessage 8cmz6gLGJD7sTcjhkS6xG3CKkf68zKQHqF "dfip-1-yes"
    H7LnPPnRScYON/dbAAQ7qKYJw41D2QocPghFfWfNJAMnTVYL6lPMSPESPpXPTL7Gp4rJJAnKCmfEICIS+P4G3U8=
    ```

    Other messages and comments can be posted alongside the proof as long as long as the proof and the vote is valid.

4. At the closing date or block, a simple majority of the votes, excluding neutral votes, would determine the outcome of a decision. 

### Validation

If you would like to check for your vote validity, you can use the `verifymessage` RPC. For instance, enter the following to any DeFiChain node, it should respond with either a `true` or `false`.

```sh
$ defi-cli verifymessage 8cmz6gLGJD7sTcjhkS6xG3CKkf68zKQHqF H7LnPPnRScYON/dbAAQ7qKYJw41D2QocPghFfWfNJAMnTVYL6lPMSPESPpXPTL7Gp4rJJAnKCmfEICIS+P4G3U8= "dfip-1-yes"
true
```
