# PowerController

Controller smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 initiatives and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Web3 Initiative:** [Relics](https://cartadao.io/relics)

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** PowerController

**Contract Address:** [0x9966...8D41](https://polygonscan.com/address/0x99667e3777059E792ED56e9C3ecCcF1caA708D41)

**Contract Code:** [0x9966...8D41](https://polygonscan.com/address/0x99667e3777059E792ED56e9C3ecCcF1caA708D41#code)

### Description
The PowerController smart contract is responsible for the creation and management of Power NFTs (also known as “Relic“ collectibles), which represent both voting power and the right to earn Carta Coins. When a Power NFT is purchased, it is minted on-the-fly and associated Power Coins are also mined. These Power Coins provide the holder with voting power and the ability to participate in votes on the platform.

Power NFTs are subject to a vesting period after they are purchased, during which they cannot be sold. After the vesting period expires, the Power NFT can be sold, at which point it will be burned along with the associated Power Coins.

Power NFTs can also be delegated, allowing their owners to keep them in a secure wallet while delegating the right to claim earnings to another individual. This separation of ownership and earnings claims increases security. Delegation can be adjusted by the NFT owner at any time.

> #### Good to Know
> The price of Power NFTs is determined by the amount of Power Coins that are bound to them. Power Coins have value because they represent ownership of liquidity in liquidity pools. When users buy Power NFTs or Power Coins, they are adding liquidity to the pools, and when they sell Power NFTs or Power Coins, they are removing liquidity from the pools.
> ***
> Power NFTs that are allocated to the pioneers, ambassadors, or for marketing purposes can never be sold. These Power NFTs may have voting and earning rights, and are intended to ensure that the holders are not motivated by financial gain, but rather by their commitment to fulfilling their duties and upholding the will of the members.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Claims the earnings of the Power NFTs held in the contract:

	function governanceClaim(
        uint256 nftId,
        uint256 pathId,
        uint256 amountOutMin
    )

Proportionally transfers a token that is hold in the contract (represented by pathId) to new holders:

	function governanceTransfer(
        uint256 pathId,
        uint256 amount,
        address[] calldata recipients,
        uint256[] calldata numerators
    )

Transfers a Power NFT held in the contract to a new holder:

	function governanceTransferNft(
        uint256 nftId,
        address recipient
    )

Sets the delay at which earnings are allocated at the earliest:

	function setClaimDelay(
        uint256 claimDelay_
    )

Sets the vesting periods for the Power NFTs:

	function setUnlockDelayBatch(
        int256[] calldata categories,
        uint256[] calldata unlockDelays
    )

Sets the hardcap. After reaching this hardcap, no more Power NFTs can be purchased:

	function setHardCap(
        uint256 hardCap_
    )
