# Appendix I: Project Rewards Tool

## Intro
Here are specifications for a way of tracking people's contributions towards a project or a speculative venture so that participants know their contributions are safely recorded, in a fair way, so that they can be appropriate  recognised, paid, or rewarded when the project achieves its aims.

## Use Case:
The primary Use Case for this tool is to recognise contributors to a speculative prototype project, primarily software developers, so that if the prototype becomes a commercially viable product, the contributors can be duly compensated for their support.

## High Level Specifications:

* The requirement is to build an online tool to track input (e.g. labour) into a project via cryptocurrency token payments, providing a transparent, immutable and secure method of accounting, resistant to fraud or hacks. 
* The tokens could have real value, e.g. backed by an existing cryptocurrency, or they could have nominal value, just tokens representing effort, which may serve some other future purpose (e.g. converted into shares in a company).
* The token will be a
* The tool will therefore offer a web based front end, which is a window into the Ethereum blockchain, with the ability to call certain methods on the Ethereum Smart contract.
* The tool will have basic Invoice Approval and Remittances functionality, as per an Accounts Payable system
* The tool will allow a user to view transaction histories, linking an Ethereum transaction ID to a specific invoice, for a specific piece of work.
* The tool will provide User Login and Authentications and allow the specification and assignment of different Roles within the system, giving permissions to use desired functionality.


#### Questions/Investigation - Smart Contracts for full Accounts Payable?

* Should the whole payments request and approval functionality take place via Smart Contracts, with the UI simply providing a window into the blockchain records.
* Or should the approval functionality be in an offline DB and only the approved transactions via Smart Contract?
* The answer to the above may depend on Gas costs (e.g. if the cost of processing every single request to the Ethereum network is too much of an overhead for a full accounts payable system)

## Proposed Implementation:
The below is just one possibility on how to go about implementing this project. Better suggestions are welcome.

1. Create the Ethereum Smart Contracts
   - BUllet
   - Next Bullet
1. Next step
   - Next Bullet


## Lower level Requirements, Deails, Thoughts, Questions:

#### How will the tool be used in practice? E.g. What will be the rewards process/workflow?

* Pre-agree a price for a work ticket (e.g. through bidding or through some other price setting method)
* Pre-agree conditions, payments, and penalties
* Do the work and meet the conditions
* Submit Invoice (e.g. this could be automated via a git-hook - the commit reference may contain the required ticket info to trigger the appropriate invoice)
* Invoice approval process 
* Immediate remittance via Ethereum blockchain.
* Note: would need some way of requesting payment back from the Payee in the event of overpayments / mistakes


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
* View everyones contributions or just your own? Privacy / secrecy / Transparency?

User Logins and Authentication:


----------
[CONTENTS](README.md) | [< BACK](references.md)
