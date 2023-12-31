## AAVE Risk Management


## Introduction

The Aave protocol is a popular liquidity protocol on Ethereum. It allows users to supply and borrow crypto assets 
on Ethereum. Active borrowers who are willing to pay interest have access to pools of crypto assets supplied by 
users who seek yield on their savings.

DeFi is all about liquidity; without it, the whole ecosystem would grind to a halt. And because of the way that different 
components in DeFi are interconnected, any risks in one area can quickly flow through the entire system. With the 
market growing so quickly, it's more important than ever to remember that there are many risks associated with DeFi.

Aave's risk framework provides a comprehensive guide for the different risks associated 
with the protocol as well as the different ways to mitigate them. By taking into account market, counterparty, and 
smart contract risks, Aave Protocol aims to set a higher standard for risk management within the DeFi space.

The team at Aave constantly strives to make the protocol safer.


    


---
## Evaluation





##### Which of these are the risks that Aave team tries to mitigate?  
     
- [x]  Market Risks
- [x]  Smart Contract Risks
- [ ]  Change in Price of ETH
- [x]  Counter-Party Risks

    


---
## Risk by Addition of a new token

Aave enables users to supply and borrow digital assets through liquidity pools. Suppliers receive protocol-issued 
aTokens, holding the user’s supplied assets and accrued yield.

The collateral secures each borrow and acts as a risk mitigation tool against default.

Following are the risks associated with the addition of tokens -

### Increase in gas price
Adding of a new token can lead to increase in gas prices for most of the protocol operations. So it's important to 
know the impact on the protocol. 

### The protocol risk of insolvency      
  Adding a new token involves the risk of insolvency. While adding new tokens the Aave Community considers the 
  following important points -      
    1. Only the assets with best risk profiles should be supported as collateral
    2. Riskier assets should only be enabled as collateral in isolation mode
    3. New assets with higher risk and lower liquidity should be only considered listed in Isolation mode (for both borrow and collateral use)

### Centralisation risk      
A centralized asset accepted as collateral exposes the protocol to centralization risk. The single point of failure 
risks of the underlying tokens enter into the Aave Protocol due to the centralized asset being accepted as collateral.

### Risk of collateral assets
Tokens that are enabled only for supplying and borrowing and are not usable as collateral, present lower risk for 
the protocol. Collaterals are the assets of the protocol. For solvency, these assets must remain greater than the 
liabilities borrowed from the protocol. Tokens that can only be used for borrowing should always be excessively backed 
by collateral assets (e.g., a user can supply DAI as collateral and borrow DAI in variable mode backed by DAI as collateral).

### Risk of manipulable oracles      
Assets that have risk of manipulable oracles are listed as single borrow assets. If a user borrows the mentioned asset, 
they cannot borrow any other asset (Siloed assets).

### Token Concentration(Low diversity)
If there are just a couple of tokens in the protocol, then volatilie conditions of those tokens can affect the full protocol. But by 
having many markets/pools, the risk is diversified.


    


---
## Evaluation





##### Which of these is not a risk associated with adding of a new asset?  
     
- [ ]  Increase in gas price
- [x]  Risk of adding unknown tokens
- [ ]  Risk of collateral assets
- [ ]  Risk of manipulable oracles





##### What is the best way to add new high risk assets?  
     
- [x]  New assets with higher risk and lower liquidity should be only considered listed in Isolation mode (for both borrow and collateral use)
- [ ]  New assets cannot be added
- [ ]  Allow them to be borrowed against other volatile assets
- [ ]  Allow them to be used as collateral for stable coins

    


---
## Types of Risks


## Smart contract risk
The focus of smart contract risk is on assessing the security of the code that underlies any asset. Only code that 
has been thoroughly audited by well-respected auditors is appropriate for the Aave protocol. Users are advised to 
be vigilant, as even beyond audits, smart contract risk does exist and it can never be eliminated completely.

One interesting mechanism that Aave plans to use to help reduce smart contract risk is bug bounties.

Also, to prevent hacks, Aave protocol advices to onboard the contracts with strict risk mitigation such as supply caps or isolation mode.

## Counterparty Risk
When it comes to decentralized governance models, there are varying degrees to which control over funds (or even 
attack vectors) may be given to the governing architecture. 

Counterparty risk is determined by the level of centralization within the system, which can be measured by 
things like the number of parties controlling a token's protocol, as well as the number and distribution of holders, 
and the level of trust in the entity, project, or community running the show.      

## Market Risk      
Aave assesses market risk by taking into account the size of the asset pool, as well as supply and demand. The 
market needs to have enough volume to handle any liquidations, which can lower the price of the asset. Aave uses 
average daily volume to assess liquidity risk.

The volatility risk is based on the normalized fluctuations in the token price and is calculated as the standard 
deviation of the logarithmic returns.

Tokens can be subject to sudden volatility spikes, and it is not uncommon to witness a 50% price change within a 
week or a month. When a price increase occurs, a parameter readjustment may be implemented to limit the risks of 
new operations.

Finally, Aave also considers the market capitalisation representing the size of the market and potential exposure.

Market risks are used to calibrate the model’s risk parameters. Volatility helps to define the required level of 
collateralisation. The liquidity risks are contained by liquidation incentives.


    


---
## Evaluation





##### Which of these can result in Counterparty Risk?  
     
- [ ]  Adding of a new asset
- [ ]  Bug in Smart Contract
- [x]  A whale accumulating most of the protocol's token leading to centralized governance
- [ ]  Volatility of a particulat token





##### Which of these can lead to Market Risks?  
     
- [ ]  A whale accumulating most of the protocol's token leading to centralized governance
- [x]  Volatility of a particulat token
- [ ]  Bug in Smart Contract
- [ ]  None of these

    


---
## Liquidity Risk

The liquidity of the protocol is very important as it allows for the basic protocol operations to take place, such 
as borrowing assets that are backed by collateral. It also allows users to claim supplied assets along with the 
interest that has accrued. Measuring the liquidity is done by taking into account the utilisation ratio, which is 
the amount of the reserve that is currently borrowed in relation to the Aave supply of each asset.

There are tools in place to help mitigate liquidity risk, such as the borrow interest rate model and alternative 
sources of aToken liquidity.

Aave mitigates the liquidity risk by the following two ways

### 1. Borrow Interest Rate
Aave's interest rate algorithm is designed to carefully manage liquidity risk and optimize utilization. The borrow 
interest rates are derived from the Utilisation Rate, which is an indicator of the availability of capital within 
the pool. The interest rate model manages liquidity risk in the protocol by incentivizing users to support liquidity: When capital is available, 
low interest rates encourage borrowing. When capital is scarce, high interest rates encourage repayments of debt and additional supplying.

### 2. aToken Liquidity
In order to mitigate aTokens' liquidity risk, Aave has set up liquidity pools on Uniswap and Balancer, as well as 
the Aave Curve pool. This provides users with alternative sources of liquidity, enabling them to redeem aTokens 
even when there is no liquidity available in the protocol.


    


---
## External Audits & Analysis

As the Aave ecosystem expands, so do the potential risks and rewards. Security is always our top priority, and we 
have put in place best practices like automated testing and independent security audits to mitigate risk. Below you 
will find a summary of our recent security audits, which cover all aspects of the Aave protocol including smart 
contracts, algorithms, stress testing, and governance. Audit reports are available on GitHub.

### Security & Audits
Below are the links to all audit reports and formal verification for Aave V3

#### Audit Round 1

| Auditor       | Date       | Report                                                                                                               |
| ------------- | ---------- | -------------------------------------------------------------------------------------------------------------------- |
| ABDK          | 27-01-2022 | [ABDK\_AaveV3](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022\_ABDK\_AaveV3.pdf)                 |
| OpenZeppelin  | 01-11-2021 | [OpenZeppelin\_AaveV3](https://github.com/aave/aave-v3-core/blob/master/audits/01-11-2021\_OpenZeppelin\_AaveV3.pdf) |
| Trail of Bits | 07-01-2022 | [TrailOfBits\_AaveV3](https://github.com/aave/aave-v3-core/blob/master/audits/07-01-2022\_TrailOfBits\_AaveV3.pdf)   |
| Peckshield    | 14-01-2022 | [PeckShield\_AaveV3](https://github.com/aave/aave-v3-core/blob/master/audits/07-01-2022\_TrailOfBits\_AaveV3.pdf)    |



#### Audit Round 2

| Auditor    | Date       | Report                                                                                                           |
| ---------- | ---------- | ---------------------------------------------------------------------------------------------------------------- |
| SigmaPrime | 27-01-2022 | [SigmaPrime\_AaveV3](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022\_SigmaPrime\_AaveV3.pdf) |

### Formal Verification
Formal verification by [Certora](https://github.com/aave/aave-v3-core/blob/master/Certora/certora/Verification\_Report.pdf)


    


---
## Evaluation





##### How does AAVE protect its protocol from Liquidity related risks?  
     
- [ ]  Balancing the Borrow Interest Rate bases on demand
- [ ]  Using stable coins
- [x]  Aave has set up liquidity pools on Uniswap and Balancer, as well as the Aave Curve pool that provides users with alternative sources of liquidity
- [ ]  By code reviews





##### What is the difference in Code review and External Audit?  
     
- [ ]  External audits are performaed by the team members whereas code reviews are performed by external teams
- [x]  External audits are performaed by external teams whereas code reviews are performed by the team members
- [ ]  They are one as the same
- [ ]  No bugs are reported in audits, but bugs are reported in code reviews

    


---
## Your Info





| Label | Type | Required |
| ----------- | ----------- | ---- |
| Nick Name        | PublicShortInput   |  true    |




    

