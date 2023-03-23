# SoulBoundController

Controller smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Project:** [SoulBound](https://cartadao.io/soulbound)

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** SoulBoundController

**Contract Address:** [0x4f11...534F](https://polygonscan.com/address/0x4f1171ea08EC987dDDD06Fe3909dbA4B0C4b534F)

**Contract Code:** [0x4f11...534F](https://polygonscan.com/address/0x4f1171ea08EC987dDDD06Fe3909dbA4B0C4b534F#code)

### Description
The SoulBoundController smart contract mints a non-transferable SoulBound NFT (collectible) that is assigned to the user. Each user can hold only one SoulBound NFT on his account.

As a main function, the user can generate any number of characters by paying for them a certain amount in Carta Coins or other currencies that the platform allows. The paid amount flows into the treasury as well as into the earnings pools, shared by all members. The more characters a user generates, the higher his entitlement to the distribution of the earnings assigned to the SoulBoundController.

The characters are provided with traits specified by the user. The characters themselves are assigned to the NFT and are therefore not transferable. The user can choose a character as an avatar - which then becomes the main character for his SoulBound NFT.

The SoulBound NFTs have the purpose of token gating to allow their holders access to various exclusives. A mapping between the user profile of a social account (e.g. discord) and the NFT allows external applications to check rights in order to grant access. For this purpose, the user registers his social account through the SoulBoundController smart contract.

SoulBound NFTs can also be delegated, allowing their owners to keep them in a secure wallet while delegating the right to claim earnings to another individual. This separation of ownership and earnings claims increases security. Delegation can be adjusted by the NFT owner at any time.

As a tertiary function, the SoulBoundController serves as holder for raffled NFTs of other internal projects whose earning rights have been delegated to the winners.

> #### Good to Know
> SoulBound collectibles serve as a ticket to valuable giveaways and more.
> ***
> To participate, [join our discord](https://discord.com/invite/cBfnKgDkGb) community, [register your username](https://cartadao.io/soulbound) and take part in our regular giveaways. 


## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the share of earnings that is parked in treasury for marketing purposes. The difference is allocated as earnings.

	function setTreasuryPermille(
        uint256 treasuryPermille_
    )

Sets the character purchase price (in Carta Coin):

	function setPriceToken(
        uint256 priceToken_
    )

Sets the maximum number of traits that can be selected per character:

	function setTraitLengthMax(
        uint256 traitLengthMax_
    )

Sets the delay at which earnings are allocated at the earliest:

	function setClaimDelay(
        uint256 claimDelay_
    )