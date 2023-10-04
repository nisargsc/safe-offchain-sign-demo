# Safe Offchain signature demo

## Overview
This is a demo repo for the Safe Wallet off-chain signature functionality with Buildbear. We have developed three API end points on Buildbear backend API. 
`POST /plugin/safe/proposeTransaction`: Used to propose the transaction fist time, backend will store the transaction in db
`GET /plugin/safe/getTransaction`: Used to get the transaction from the backend db.
`POST /plugin/safe/addSignature`: Add sign to the db after creating the sign.

## Flow
After deploying the safe Account, Owner will create the transaction using safeSdk and will use `proposeTransaction` API to send the transaction to backend db.
Other owners will use `getTransaction` and `addSignature` to add their signatures to te transaction.
Finally one Owner will use the `getTransaction` API and `safeUtils.getExecTxn()` utils method to get the transaction instance to execute.

## How to run?
After cloning the repo do `yarn` to install all the dependencies. After that to run the script do `yarn start`