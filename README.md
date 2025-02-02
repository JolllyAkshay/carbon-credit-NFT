# C-Block: Marketplace for carbon-credit NFTs from forestry projects

<h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1t5-R_76JmHLmhAaG2n9Sf1ApvbymEyog)
  <a name="logo" href="https://drive.google.com/file/d/1t5-R_76JmHLmhAaG2n9Sf1ApvbymEyog/view?usp=sharing" alt="Carbon Credit Marketplace" width="200"></a>
  <br>
  C-Block: Decentralised Carbon Credit Marketplace
  </h4>
</div>
<p><font size="3">
This Repo is desgiend to serve as a platform for the development of a decentralised market place for Carbon Credit transactions. Our aim behind the project is to have a decentralised, democratic and transparent platform where farmrers, landowners may interact with Large industries and institutional investors interested in the voluntary carbon capture projects.  
  
  <h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1WoPft4sMm-cRpxaCM3tY7Ure2ErbIXOa)

  </h4>
</div>
<p><font size="3">
Carbon offsets in a Nut Shell, is the reduction or removal of emissions of carbon dioxide or other greenhouse gases made in order to compensate for emissions made elsewhere. Broad Picture, it allows industries to reduce their overall carbon footprint by investing in projects that can offer measurable Carbon Capture from the environment. 
    
  <h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1MHjvzIQZmmL7kvVh5ai3JE52hOukQEzo)

## Infrastructure / Solution / Approach
    
  <h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1csoSuH-r4chefz4xfpMfNUeBXVe0typl)

  </h4>
    
  <h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1wfObw7mFrq9fMmkYQ7E9CVGaqOYF3v4Z)

  </h4>
    

</div>
<p><font size="3">

Our solution to challenge the existing highly centralised marketplace is to implement a decentralised protocol as shown above. THe landowners could come to our platform with their projects. A DAO of auditors and domain experts would analyse the credibility of the project. Once a significant majority is reached, the project would be minted as a ERC 721 NFT compatible with the Ethereum blockchain. A deterministic (decided by the DAO) number of ERC 20 tokens would be minted for each project. These ERC 20 token would represent a unit portion of the Carbon Capturd by the Project. Industries / Institutions / Individuals would then b able to buy these ERC20 tokens represnting a unit of Carbon Offset.  
  
    
## Prerequisites

Please install or have installed the following:

- Nodejs and npm
- Python
- Brownie 


# Usage / Implementation
  
There are 2 types of NFTs here. 
1. `SimpleCollectibles.sol`
2. `AdvancedCollectibles.sol`

The simple collectibles work on a local network,  however the advanced requires a testnet. We default to rinkeby since that seems to be the testing standard for NFT platforms. You will need testnet rinkeby ETH and testnet Rinkeby LINK. You can find faucets for both in the [Chainlink documentation](https://docs.chain.link/docs/link-token-contracts#rinkeby). 

# We will use the Advanced Collections contract implementation. Each project is associated with an NFT, containing an image and a json file. This json file contains:
  - informations relative to the asset: 
    - geolocation
    - type of project 
    - soil main composition
    - main type of trees
    - ...
  
  - informations relative to the ERC20 tokens that will be traded as "shares" of this asset:
    - ERC20 token address
    - ERC20 token total supply
    - ERC20 token decimals

Inforamtions relative to the asset are randomly generated from a database of event we have build. They will be expanded with the addition of real projects.
  
---
  
You'll need [testnet Rinkeby](https://faucet.rinkeby.io/) and [testnet LINK](https://rinkeby.chain.link/) in the wallet associated with your private key. 

```
brownie run scripts/advanced_collectible/deploy_advanced.py --network rinkeby
brownie run scripts/advanced_collectible/create_collectible.py --network rinkeby
```
Then:
```
brownie run scripts/advanced_collectible/create_metadata.py --network rinkeby
brownie run scripts/advanced_collectible/set_tokenuri.py --network rinkeby
```

## Resources Used

The project is created in parts towards the submission for the Chainlink Hackathon. A great thanks to Patrick Collins and the whole Chainlink Hackathon team for the essential tutorials and support provided during the project execution. 

* [Chainlink Documentation](https://docs.chain.link/docs)
* [Chainlink Hackathon Discord](https://discord.gg/2YHSAey
* Check out the [Chainlink documentation](https://docs.chain.link/docs) to get started from any level of smart contract engineering. 
* Check out the other [Brownie mixes](https://github.com/brownie-mix/) that can be used as a starting point for your own contracts. They also provide example code to help you get started.
* ["Getting Started with Brownie"](https://medium.com/@iamdefinitelyahuman/getting-started-with-brownie-part-1-9b2181f4cb99) is a good tutorial to help you familiarize yourself with Brownie.
* For more in-depth information, read the [Brownie documentation](https://eth-brownie.readthedocs.io/en/stable/).

## The Path Ahead
Though, we have made substantial progress towards our end goal of a decentralised Carbon Credit Marketplace, there is still 'Miles to go'. Some of the updates / initiatives that we have in the works - 
* Implementing collaboration with off chain and other on chain Carbon Credit Marketplace to further improve the liquidity within the Market. 
* To plan for the future - We understand the current voluntary Carbon Credit Market will grow substantially if not exponentially in the coming future. This would call for the current model to expnand to ther avenues of Carbon Capture, say industrial carbon capture, renewable energy projects, advanced technological projects.
* Since, the active Carbon Capture projects could be highly volatile in terms of actual output. We need to implement a methodology to source, manage and create a pool or repository of Carbon Credits to cover any potential shortfall in production. 

  <h1 align="center">
  
  ![image](https://drive.google.com/uc?export=view&id=1UCpQn7Cb-843Uiwee69sD6rwGlGlLTHz)

  </h4>  
## License

This project is licensed under the [MIT license](LICENSE).

