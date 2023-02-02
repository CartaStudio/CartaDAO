# GenerativeController

Controller smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Project:** [AGI](https://cartadao.io/agi)

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** GenerativeController

**Contract Address:** [0xaeC2...6f2F](https://polygonscan.com/address/0xaeC20dD10d10b5598224942d71458843aa076f2F)

**Contract Code:** [0xaeC2...6f2F](https://polygonscan.com/address/0xaeC20dD10d10b5598224942d71458843aa076f2F#code)

### Description
The GenerativeController smart contract is an extension of the NFT smart contract that allows users to buy and sell generative NFTs on the built-in DEX, as well as claim Carta Coins as rewards for holding them.

Generative NFTs are locked (cannot be sold) for a set period of time (vesting) after they are purchased, after which they can be sold and returned to the DEX for others to purchase.

Generative NFTs can also be delegated, allowing their owners to keep the NFTs in a secure wallet (such as a cold wallet) and delegate the rights to claim earnings to someone else (the delegatee). This increases security by separating ownership of the NFT from the ability to claim earnings. Delegation can be adjusted by the NFT owner at any time.

> #### Good to Know
> The value of a generative NFT is based on the sum of the values of its individual traits, which are also NFTs. These trait NFTs are bound to Carta Coin liquidity through the NFT DEX, allowing trait NFTs as well as generative NFTs to have a defined price for buying and selling on the platform.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the vesting periods for the generative NFTs:

	function setUnlockDelayBatch(
        int256[] calldata categories,
        uint256[] calldata unlockDelays
    )
