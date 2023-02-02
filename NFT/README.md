# NFT

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** NFT

**Contract Address:** [0xf423...4515](https://polygonscan.com/address/0xf423F0afC67cBE631714Ef68C03e21a1ff324515)

**Contract Code:** [0xf423...4515](https://polygonscan.com/address/0xf423F0afC67cBE631714Ef68C03e21a1ff324515#code)

### Description
The NFT smart contract implements the ERC1155 protocol and extends the basic functionality of NFTs by adding controller-specific data.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the metadata:

	function setMetadata(
        string calldata name_,
        string calldata symbol_,
        string calldata uriPrefix_,
        string calldata uriSuffix_
    )

Sets the masterchief:

	function setMasterchief(
        address masterchief_
    )
