# GovernanceToken

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** GovernanceToken

**Contract Address:** [0x2F10...3839](https://polygonscan.com/token/0x2F106058e3130A7a146f7D26FD582ebB883c3839)

**Contract Code:** [0x2F10...3839](https://polygonscan.com/address/0x2F106058e3130A7a146f7D26FD582ebB883c3839#code)

### Description
The GovernanceToken smart contract is an ERC-20 token that represents the Power Coin within Carta DAO. It is designed to keep track of votes and vote delegation through the use of the ERC20Votes extension. It has been modified to allow only whitelisted smart contracts to hold these tokens and includes built-in mechanisms for minting and burning tokens through the Masterchief smart contract.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions


Sets the masterchief:

	function setMasterchief(
        address masterchief_
    )
