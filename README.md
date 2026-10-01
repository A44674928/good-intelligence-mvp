# Good Intelligence (an Empty.Domains product) MVP/Alpha  (OLD, system has passed Beta stage and now Production)

<p align="center">
  <img src="Good-Intelligence-Logo.png" alt="Good Intelligence, an Empty.Domains product" />
</p>

## Introduction

Current, reputable & actionable intel for digital currency traders and investors. 

Good Intelligence (an Empty.Domains product) is a financial intel platform. The purpose is to change the incentive model around how profitable event-driven information is shared while giving its consumers confidence in the objective nature of the information.

Users gain access by signing an Ethereum address which contains Good Intelligence tokens built using erc20 smart contract standard. This allows user identity, accounting and authentication to be offloaded to the Ethereum blockchain. Good Intelligence doesn't use more onchain and further maintains its distributed nature through an adhoc network of intel providers. Intel providers are compensated in Good Intelligence tokens.

<p align="center">
  <img src="Good-Intelligence-GUI-Dashboard.png" />
</p>

## Architecture

The present MVP/Alpha stores intel in a centralized database, further iterations may leverage distributed blob storage such as IPFS depending on the performance limitations of the solution.

The code here is only the Node.js built for the AWS Lambda functions. The majority of the Alpha involves the configurations on AWS between API Gateway, Lambda, S3, DynamoDB as well as the routing to those functions.

<p align="center">
  <img src="Good-Intelligence-Diagram.png" />
</p>

This method lays the ground work for a scalable solution which allows for additional integrations to be built making use of the API and infrastructure of Amazon.


## Access

Good Intelligence users are distinguished by a primary Ethereum address. The network checks to see if there is a balance of Good Intelligence tokens in their address and grants the user access if they are able to sign the address. Signing proves ownership of the address. This can be accomplished through a manual process or automated process using browser extensions such as Metamask.

## Ranking

Rank in Good Intelligence determines how soon you are able to access financial intel.

Good Intelligence users are subject to an ongoing Proof of Activity analysis to determine their ranking. The formula is posted here for reference.

<p align="center">
  <img src="Good-Intelligence-Ranking-Formula.png" />
</p>

The Lambda functions here currently omit the implementations of the formula, and instead are placeholders to provide the glue for the system architecture, giving code for the API Gateway routes to execute and the DynamoDB methods to write to. Given the integral nature of the Good Intelligence tokens to the Good Intelligence system even though the contract had not been deployed on mainnet during testing, a different deployed contract signature is implemented for analysis and references to it may be seen in the code.
