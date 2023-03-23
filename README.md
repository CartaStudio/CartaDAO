
# Carta DAO

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

[https://cartadao.io](https://cartadao.io)

## Smart Contracts

### Base Smart Contracts

#### Masterchief
Acts as a control center for various tasks, including distribution of Carta Coin earnings, buying and selling of Power Coins, coordination of shared liquidity, and DEX token swaps. [Read More](Masterchief)


#### Timelock
Adds a delay for the execution of governance decisions, requiring a queue step before execution. [Read More](Timelock)

#### Token
A modified ERC-20 smart contract representing the Carta Coin, with built-in mechanisms for minting and burning tokens through the Masterchief smart contract.  [Read More](Token)

#### GovernanceToken
A modified ERC-20 smart contract representing the Power Coin, with the ability to track votes and vote delegation. [Read More](GovernanceToken)

#### NFT
An ERC-1155 smart contract extending the basic functionality of NFTs with controller-specific data, and allowing only controllers to access and modify the NFTs. [Read More](NFT)

#### NiftyswapExchange20
A decentralized token swap protocol for ERC-1155 tokens, with DEX functionality and built-in royalty features. [Read More](NiftyswapExchange20)

#### Deputy
A smart contract that makes proposals on behalf of Carta Studio, with the potential to be replaced by a vote allowing all eligible members to make proposals. [Read More](Deputy)

#### Utils
A helper smart contract with read-only functionality, providing structured asset data to the view. [Read More](Utils)


#### UniswapV2Pair
A smart contract created by the Quickswap v2 protocol, allowing for the swapping of ERC-20 tokens. Manages the liquidity of Carta Coin paired with USDC stablecoin. [Read More](UniswapV2Pair)

***

### Controller Smart Contracts

#### GovernorController
Responsible for managing the governance process within Carta DAO. [Read More](GovernorController)

#### PowerController
Allows the buying and selling of Power NFTs, which have both voting power and the ability to earn Carta Coins. [Read More](PowerController)

#### GenerativeController
Allows the buying and selling of Generative NFTs through a built-in DEX, and enables the claiming of rewards in the form of Carta Coins for holding them. [Read More](GenerativeController)

#### SoulBoundController
Allows SoulBound NFTs to be minted for token gating, character generation, and claiming Carta Coin rewards for generating them.[Read More](SoulBoundController)
