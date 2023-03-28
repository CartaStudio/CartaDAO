# GovernorController

Controller smart contract of the [Carta DAO](https://cartadao.io) protocol.

[https://cartadao.io](https://cartadao.io)

Carta DAO is a decentralized platform that invites users to explore innovative web3 initiatives and earn Carta Coins through holding collectibles and participating in votes.

## Smart Contract

**Web3 Initiative:** [Proposals](https://cartadao.io/proposals)

**Protocol:** [Carta DAO](https://cartadao.io)

**Contract Name:** GovernorController

**Contract Address:** [0x9E37...E60D](https://polygonscan.com/address/0x9E377D9498F62e7c9A6ffbdE43D63318733CE60D)

**Contract Code:** [0x9E37...E60D](https://polygonscan.com/address/0x9E377D9498F62e7c9A6ffbdE43D63318733CE60D#code)

### Description
The GovernorController smart contract enables the deployment of on-chain voting on the Carta DAO platform. It is based on the [Governor](https://docs.openzeppelin.com/contracts/4.x/api/governance) smart contract provided by OpenZeppelin, which is a widely-used and trusted tool for implementing governance mechanisms in decentralized systems.

By using this smart contract, Carta DAO ensures that its voting process is transparent, secure, and fair. To encourage user engagement and involvement in the governance processes of Carta DAO, a system of rewards in the form of Carta Coins has been implemented. These rewards are not directly tied to the outcome of the vote, in order to prevent distorted voting.

To participate in the voting process on Carta DAO, users need to have voting power. This can be obtained by holding Power Coins or by owning "Relics" collectibles, which include voting power as a feature.

> #### Good to Know
> Only the [Deputy](todo) smart contract is currently able to make proposals on Carta DAO due to the technical nature of the votes, which include executable smart contract code. Once the correct usage is understood by all members, a vote will be held to determine if this restriction should be lifted, allowing all eligible members to make proposals.
> ***
> The Creator has the ability to decline proposals, with the exception of the proposal to select a [new Creator](todo) (on Masterchief), which can be made by any member. This system ensures that only legitimate proposals are implemented and prevents overreaching by stakeholders.


## Executable Code

To create a proposal, you can follow the instructions in the [OpenZepplin on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance) section:

[Create a Proposal](https://docs.openzeppelin.com/contracts/4.x/governance#create_a_proposal)

The following smart contract functions can be proposed for execution provided you have the required rights:

#### Functions

Sets the delay at which earnings are allocated at the earliest:

	function setClaimDelay(
        uint256 claimDelay_
    )

Sets the voting delay before the start of the votes:

	function setVotingDelay(
        uint256 newVotingDelay
    )

Sets the voting period:

	function setVotingPeriod(
        uint256 newVotingPeriod
    )

Sets the minimum amount of voting power that must be held in order to make proposals:

	function setProposalThreshold(
        uint256 newProposalThreshold
    )

Sets the current quorum numerator:

	function updateQuorumNumerator(
        uint256 newQuorumNumerator
    )
