# Appendix I: Project Rewards Tool

## Intro:
Here are specifications for a way of tracking people's contributions towards a project or a speculative venture so that participants know their contributions are safely recorded, in a fair way, so that they can be appropriate  recognised, paid, or rewarded when the project achieves its aims.

This should be the ideal mini-project for a developer to get their teeth into doing practical applications of Blockchain, Cryptocurrency and Smart Contract technologies.

## Use Case:
The primary Use Case for this tool is to recognise contributors to a speculative prototype project, primarily software developers, so that if the prototype becomes a commercially viable product, the contributors can be duly compensated for their support.

## High Level Specifications:

* The requirement is to build an online tool to track input (e.g. labour) into a project via cryptocurrency token payments, providing a transparent, immutable and secure method of accounting, resistant to fraud or hacks. 
* The tokens could have real value, e.g. backed by an existing cryptocurrency, or they could have nominal value, just tokens representing effort, which may serve some other future purpose (e.g. converted into shares in a company).
* The tool will therefore offer a web based front end, which is a window into the Ethereum Blockchain, with the ability to call certain methods on the Ethereum Smart contract.
* The tool will have basic Invoice Approval and Remittances functionality, as per an Accounts Payable system
* The tool will allow a user to view transaction histories, linking an Ethereum transaction ID to a specific invoice, for a specific piece of work.
* The tool will provide User Login and Authentications and allow the specification and assignment of different Roles within the system, giving permissions to use desired functionality.


#### Questions/Investigation - Smart Contracts for full Accounts Payable?

* Should the whole payments request and approval functionality take place via Smart Contracts, with the UI simply providing a window into the Blockchain records.
* Or should the approval functionality be in an offline DB and only the approved transactions via Smart Contract?
* The answer to the above may depend on Gas costs (e.g. if the cost of processing every single request to the Ethereum network is too much of an overhead for a full accounts payable system)

## Proposed Implementation:
The below is just one possibility on how to go about implementing this project. Better suggestions are welcome.

#### Build the dApp (Distributed Application)
1. Create the Ethereum Smart Contracts:
   - Create the main token contract, using [ERC20 Standards](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md) exposing methods to do 'Accounts Payable' functionality (invoice submission, invoice approvals, remittances)
   - Once the Smart Contracts are up and running, we could start using them for this 'Projects Rewards Tool' project by interacting with the contracts via the [Ethereum Mist Wallet](https://github.com/ethereum/mist/releases), [MetaMask](https://metamask.io/), or simply through an [Ethereum GETH Command Line Console](https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options)
   - The Ethereum Smart Contracts can be built using [Solidity](https://solidity.readthedocs.io/en/develop/), [YouTube Tutorial](https://www.youtube.com/channel/UCaWes1eWQ9TbzA695gl_PtA)
   - The Smart Contracts can be built and tested using [Truffle Framework](http://truffleframework.com/) and [Remix IDE](https://remix.ethereum.org/)
   - For many, this will be their first time working with Ethereum Smart Contracts. We will inevitably run into problems, but this will help us to learn, refine and improve
   - One important thing to learn would be the likely cost of Ethereum Gas to record and manage transactions as we scale (see [Gas Price](https://etherscan.io/chart/gasprice) and [Gas Station Calculators](https://ethgasstation.info/)).
   - A repos has been created for storing smart contracts at: https://github.com/ScrutiNews/project-rewards-contracts
1. Next, we could build a fancy front-end User Interface (UI) to interface with the Smart Contracts:
   - Should we use the [Truffle Framework](http://truffleframework.com/) or build our own using a more traditional technical stack combined with the [Web3.js](https://github.com/ethereum/web3.js/) JavaScript API tool?
   - The fancy UI will make it easy for people to manage invoice submission, approvals and emittances, as well as interrogation of the Ethereum Blockchain to do things like view balances and transactions history. It wall also manage user login/authentication and roles, as well as providing customisable guideline information and configuration options.
1. Tinker with other Smart Contract Platforms to evaluate whether Ethereum is the most suitable for our needs:
   - For Micro-Payments, maybe something like [IOTA](https://iota.org/) or [NANO/Raiblocks](https://raiblocks.net/) would serve us better, or perhaps we should look at [NEO](https://neo.org/) where Smart Contracts can be written in any language? While Ethereum is the most mature and wildly used Blockchain platform, there are a number of platforms to consider.
   
#### Contributors & Legals:
Some kind of legal document/agreement would need to be created to ensure our mutual obligations are contractually understood and agreed.  Perhaps the signing of agreements can also be done via Smart Contracts?


## Lower Level Requirements, Details, Thoughts, Questions:

#### How will the tool be used in practice? E.g. What will be the rewards process/workflow?

* Pre-agree a price for a work ticket (e.g. through bidding or through some other price setting method)
* Pre-agree conditions, payments, and penalties
* Do the work and meet the conditions
* Submit Invoice (e.g. this could be automated via a git-hook - the commit reference may contain the required ticket info to trigger the appropriate invoice)
* Invoice approval process 
* Immediate remittance via Ethereum Blockchain.
* Note: would need some way of requesting payment back from the Payee in the event of overpayments / mistakes; would every micro-contribution be invoiced, or would they be done in weekly batches?


#### Areas of functionality:
* User creation, Logins and Authentication
* Roles: Admin; CanAuthoriseRemittance; CanSubmitInvoice; CanApproveInvoice
* Guides to Payments
* A means of pre-agreeing and setting the value of a discrete piece of work (e.g. a ticket) - assume that it is only payable once it has met some sort of acceptance criteria.
* Transaction views, for users and admin.
* Configuration Area
* Links to project pages, what we're actually working on etc.
* Integrations (e.g. git-hooks)
* Notifications & confirmation emails
* Upload evidence of work?
* View everyone's contributions or just your own? Privacy / secrecy / Transparency?

*Consider the above as a work-in-progress, these are ideas only. More fleshing out to be done.

## Current Status & Progress:
* 25th February 2018 - This document is created, next step by John Durrant is to tinker with Ethereum Smart Contracts and the Truffle Framework.



----------
[CONTENTS](README.md) | [< BACK](references.md)
