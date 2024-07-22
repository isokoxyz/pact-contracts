# Isoko Pact Contracts

This repository contains Isoko's pact contracts. 

## Upgrade Handler
upgrade-handler.pact is the pact contract built for kadcar's upgradability used by in-house built oracle, [Ready2Render (R2R)](https://github.com/isokoxyz/R2R.git) to perform NFT upgrades by combining the assets of two NFTs together utilizing the Blender Python Module

This contract utilizes a defpact that interacts with isoko-royalty-policy to lock the NFT from being accessible before writing the upgrade blueprint to the blockchain.
The steps of the defpact:
* Verify installed capabilities
* Write upgrade blueprint data to the blueprints table
* Unlock the NFT in isoko-royalty-policy
* Set the status of the upgrade to completed
* Return the completed upgrade blueprint
