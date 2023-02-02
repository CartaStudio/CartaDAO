# Token

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** Token

**Contract Address:** [0x087E...DA85](https://polygonscan.com/token/0x087E68b5B53cfa25D7F200D24EA9E0554382DA85)

**Contract Code:** [polygonscantodo](https://polygonscan.com/address/0x087E68b5B53cfa25D7F200D24EA9E0554382DA85#code)

### Description
The Token smart contract is an ERC-20 smart contract that represents the Carta Coin, the main protocol and earning token for the Carta DAO platform. It has been modified to allow only whitelisted smart contracts to hold these tokens and includes built-in mechanisms for minting and burning tokens through the Masterchief smart contract.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the allowance of a contract address that can hold this token:

	function setWhitelist(
        address to,
        bool allowed
    )

Sets the masterchief:

	function setMasterchief(
        address masterchief_
    )
