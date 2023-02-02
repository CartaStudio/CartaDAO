# Masterchief

Base smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 projects and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** Masterchief

**Contract Address:** [0x9b6C...7D46](https://polygonscan.com/address/0x9b6C444839c7D0B3a978Eac037f7b1353C047D46)

**Contract Code:** [0x9b6C...7D46](https://polygonscan.com/address/0x9b6C444839c7D0B3a978Eac037f7b1353C047D46#code)

### Description
The Masterchief smart contract is at the heart of the Carta DAO platform, acting as a control center for various tasks. It is responsible for tracking and managing the distribution of Carta Coin earnings, enabling the buying and selling of Power Coins, coordinating shared liquidity, and enabling DEX token swaps. It also has built-in mechanisms for minting and burning tokens on behalf of the controllers.

## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the parameters of the controllers:

	function setControllerBatch(
		address[] calldata controllers_,
		uint256[] calldata numerators,
		bytes4[][] calldata selectors_,
		bool[][] calldata selectorsAllowed,
		int256[] calldata tokenAmounts
	)

Sets the half-life of the protocol earning token:

	function setHalfLife(
		uint256 halfLife_
	)

Sets the creator empowering the protocol. Can be proposed at any time by anyone with minimal voting power:

	function setCreator(
		address creator_
	)

The deputy who makes proposals on behalf of the community. Can also be address zero, in order not to designate a specific deputy:

	function setDeputy(
		address deputy_
	)

Sets a selector who must be necessarily proposed by the deputy:

	function setDeputySelector(
		bytes4 selector_,
		bool value
	)

Adds a token path allowed for payments and withdrawals:

	function addPath(
		address[] calldata path
	)

Sets the router specified for token swaps:

	function setRouter(
		IRouter router_
	)

Sets the sales tax designated for the governance token:

	function setSellTaxPermille(
		uint256 sellTaxPermille_
	)

Sets the ratios that control the rebalance of the liquidity provided.

	function setRebalancePermille(
		uint256[2] memory rebalancePermille_
	)

Sets the masterchief smart contract, which replaces the contract described here:

	function setMasterchief(
		Masterchief masterchief_
	)

***

The following init function could only be executed once during the setup of the protocol:

	function init(
		address governor_,
		IGovernanceToken governanceToken_,
		address deputy_
	)
