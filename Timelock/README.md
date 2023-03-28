# Timelock

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 initiatives and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** Timelock

**Contract Address:** [0x2885...1204](https://polygonscan.com/address/0x2885Ae3467F6422D55fC838697b0568e2dD01204)

**Contract Code:** [0x2885...1204](https://polygonscan.com/address/0x2885Ae3467F6422D55fC838697b0568e2dD01204#code)

### Description
The Timelock smart contract is used to implement a delay before governance decisions are executed on the Carta DAO platform. When a vote reaches the required quorum, the decision is added to a queue and is only executed by the Timelock contract after a certain threshold of time has passed. This adds an extra layer of security and allows for more careful consideration of proposals before they are implemented.

The Timelock contract is responsible for holding the assets that are being governed and for executing the proposals once the delay has expired.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Updates the delay:

	function updateDelay(
        uint newDelay
    )
