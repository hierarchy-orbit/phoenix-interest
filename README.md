# phoenix-glacier
phoenixIdentity bearing interest in an escrow forms a Glacier. phoenixIdentity is a protocol layer in between the Ethereum network and individual identity applications. This interoperability challenges by enabling any identity-driven application to leverage un-opinionated identity management. A digital identity can be viewed as an omnibus account, containing more information about an identity than any individual identity application could. 

This omnibus identity is resolvable to an unlimited number of sub-identities called Resolvers. Resolvers recognize identities by any of their Associated Addresses. The protocol allows for an atomic entity, the Identity, to be resolvable to abstract data structures, the Resolvers. The protocol revolves around claiming an Identity and managing Associated Addresses and Resolvers. Identities delegate much of this responsibility to one or more Providers. Provider smart contracts or addresses may add and remove Resolvers indiscriminately, but may only add and remove Associated Addresses or other Providers with the appropriate permissions.

# Project Details
An Ethereum smart contract on top of Phoenix phoenixIdentity that allows a certain percentage of interest on a defined principal amount, in PHNX, to accrue and be charged (or paid) to a wallet tied to a phoenixIdentityID, and then for that balance to automatically be withdrawn (or paid). The smart contract will guarantee that the money is in the account by enforcing an escrow of the accruing payment within the wallet, thus eliminating payment default, or fraud from institutions. This utility smart contract will power charging interest in many future savings, lending, credit, and mortgage Phoenix dApps. There will be Layer-3 dApps and Layer-4 APIs that hook into this utility smart contract function.

# Background:
* The market for interest bearing notes and accounts is huge globally
* The market for interest paying debt products is even larger globally
* One of the largest problems facing the lending markets is default; in the student loan market alone, 22% of all borrowers default on their payments every year
* From 2009-2017, nearly 500 banks failed in the U.S. costing the FDIC over $75 Billion to make clients whole
* By holding interest from an issuer or borrower in an escrow within a phoenixIdentity, counterparties can eliminate fraud, default, and validate all terms on-chain
# Features:
* Create Interest Rate - set a defined interest rate from 0%-100%
* Set Principal Amount - set the principal amount that the interest will be calculated on
* Define phoenixIdentity IDs - set the phoenixIdentity ID for the payer and the payee
* Accrual - set the accrual date for the interest payments (the default can be daily)
* Payment Schedule - set the payment schedule for the interest payments (the default can be monthly)
* End Date - set the end date, or term, of the payments. For savings the default can be infinite, for loans and credit, the default can be 1 year.
* Escrow - remove the set amount of PHNX from the phoenixIdentityID wallet to an escrow contract on the payment schedule intervals, to insure there will be no default
* Send Interest - distribute the interest PHNX from the escrow on the Payment Schedule date
* Send Principal - in the case of a debt contract, send the principal amount on the contract from the phoenixIdentity ID on the End Date.
* Confirm Payment - use the Phoenix PhoenixAuthentication smart contract to confirm receipt and payment of the interest from the payer to the payee
* Dispute - create a flag for a disputed interest payment
The interest rate, once set, cannot be edited or modified. The terms can be deleted by mutual consent of both parties via a Phoenix PhoenixAuthentication transaction.
