# NiftyswapExchange20

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** NiftyswapExchange20

**Contract Address:** [0x6f32...0bEE](https://polygonscan.com/address/0x6f32E43F1af4e37E0661a35965C7eE7dfCed0bEE)

**Contract Code:** [0x6f32...0bEE](https://polygonscan.com/address/0x6f32E43F1af4e37E0661a35965C7eE7dfCed0bEE#code)

### Description
The NiftyswapExchange20 smart contract is a decentralized exchange protocol for ERC-1155 and ERC-20 tokens, based on the original smart contract provided by [0xsequence on Github](https://github.com/0xsequence/niftyswap). It includes built-in features for buying and selling ERC-1155 tokens with bound liquidity in the form of Carta Coins and for collecting royalties.

The smart contract has been modified by Carta DAO to allow only the creator to initiate liquidity pairs and to prevent the removal of liquidity, making it a secure store of value for Carta Coins. NFTs that have bound liquidity in the form of Carta Coins can be bought and sold instantly through this smart contract.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions


Sets the royalty fee for buys and sells:

	function setRoyaltyFee(
       uint256 _fee
    )
