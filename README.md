
# About me
Independent security researcher, participated in many audits (mostly SVM & EVM-based).

# For Private Audit, DM me via
- [Twitter @KoolexC](https://twitter.com/KoolexC)

--- 
# Portfolio

## Rust & SVM-based audits (till 28th Jan, 2025 up-to-date)

### Engagements
- Pump Fun
  - no need for an introduction, I guess.
  - Report: N/A
- Pump Science
  - a Solana-based program that facilitates token launches with a
bonding curve, dynamic fee structures and automated liquidity management. It
works by using a constant product bonding curve where token and SOL reserves
dynamically adjust based on purchases.
  - Report: https://github.com/pashov/audits/blob/master/team/pdf/PumpScience-security-review_2024-12-24.pdf
- Hydration 
  - a DeFi protocol on Polkadot, offering an 'Omnipool' that combines all
  assets into a single, highly efficient trading pool, reducing slippage and increasing
  capital efficiency
  - Report: https://github.com/pashov/audits/blob/master/team/pdf/Hydration-security-review-October.pdf



### Highlights of Various Issues Found

| Protocol | Type | Severity |  Title | Summary |
| ----------- |----------- | ----------- | ----------- | ----------- |
| Pump Science   | Token Program/ATA Validation   | Critical/High        | Meteora's lock pool can be DoSed | When Pump attempts to lock LP tokens on Meteora's protocol, it uses an account's SOL balance to check if an Associated Token Account exists. An attacker can exploit this by sending SOL to prevent ATA creation, which breaks the lock pool functionality since LP tokens can't be properly stored. This enables a denial of service attack on Pump's ability to interact with Meteora's pool locking system. |
| Pump Science   | Business Logic   | Critical/High        | Bonding curve creators can manipulate the fee structure by setting start slots in the past | Bonding curve is meant to begin with high fees and gradually decrease, creators can bypass this intended progression by backdating their start slot, immediately placing them at a lower fee tier than intended.




## Competitions on Code4rena (till 6th April, 2024 up-to-date)

### Ranking
- 90-day: #20
- 2023: #30
- All-time: #67

### Participation
19 Audits

### Security Issues Found
- High-risk: 27
- Medium-risk: 22



### Highlights of Various Issues Found

| Type      | Protocol | Severity |  Title |
| ----------- | ----------- | ----------- | ----------- |
| Incorrect integration with Seaport        | Astaria   | High        | [Wrong starting price when listing on Seaport for assets that has less than 18 decimals](https://github.com/code-423n4/2023-01-astaria-findings/issues/235) 
| Claiming rewards blocked       | Ajna      | High       | [The lender won't be able to claim rewards in some cases and most of RewardsManager's methods (e.g. staking, unstaking ..etc) will revert](https://github.com/code-423n4/2023-05-ajna-findings/issues/354)       |
| Stealing NFT Assets        | Caviar   | High        | [ETHRouter doesn't revoke the ERC721's approvalForAll of the pool after the operation (e.g. sell) is finished](https://github.com/code-423n4/2023-04-caviar-findings/issues/842)       |
| Signature replay        | Biconomy   | High        | [Signature replay attack is possible in "Transaction" execution](https://github.com/code-423n4/2023-01-biconomy-findings/issues/316)       |
| Funds draining        | Astaria   | High        | [Lack of StrategyDetailsParam.vault validation allows the borrower to steal all the funds from the vault](https://github.com/code-423n4/2023-01-astaria-findings/issues/409)       |
| Withdrawal blocked temporarily        | Ethos Reserve  | Medium        | [Withdrawal functionality could possibly be blocked if a strategy's withdrawal fails](https://github.com/code-423n4/2023-02-ethos-findings/issues/671)       |
| Loss of rewards        | Redacted Cartel  | Medium        | [Loss of user rewards if reward tokens is empty when claiming rewards](https://github.com/code-423n4/2022-11-redactedcartel-findings/issues/194)       |


---
# Links:
- [Twitter Profile @KoolexC](https://twitter.com/KoolexC)
- [Code4rena Profile @Koolex](https://code4rena.com/@Koolex)
