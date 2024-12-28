# Audit Portfolio
The repository contains an index of my audit findings, CTFs I've solved and articles I have authored on smart contract security

## Profile
* [Sherlock](https://audits.sherlock.xyz/watson/parzival)
* [Codehawks](https://profiles.cyfrin.io/u/eshumanohare_cyfrin)
* [X](https://x.com/E_Manohare)

## Findings
👾 **[H] Market funds for a profile ID are set higher than the actual funds causing revert in withdrawl**
> The ReputationMarket contract ends up with lower funds if the graduation contract withdraws some market funds. Eventually if it tries to withdraw all the market funds across all the 
  profiles then this will cause a revert due to insufficient funds.
>
> https://github.com/sherlock-audit/2024-11-ethos-network-ii-judging/issues/345
---
👾 **[L] Votes are sold at a lower price than the current vote price in the market which impacts price transparency**
> The protocol sells vote at a lower price than the actual which will impact the funds the user will receive upon selling, reputation of the protocol in keeping up with a fair pricing model and will result in receiving lower protocol fees. Since the number of votes will decrease on every sell, the lower the number of votes, the higher will be the volatility on price caused by every single vote sell.
>
> https://github.com/sherlock-audit/2024-11-ethos-network-ii-judging/issues/367
---
👾 **[L] MAX_TOTAL_FEES is wrongly set to 100% which allows totalFees to exceed the expected 10% mark**
> The protocol incurs high taxes on the funds being put in the protocol on good faith for a higher return. This will break the expected 10% MAX_TOTAL_FEES invariant.
>
> https://github.com/sherlock-audit/2024-11-ethos-network-ii-judging/issues/572
---
👾 **[M] Owner unable to remove splitter when calling `LSTRewardsSplitterController::removeSplitter(...)`**
> The Owner is unable to remove an account's splitter when calling `LSTRewardsSplitterController::removeSplitter(...)`
>
> https://codehawks.cyfrin.io/c/2024-09-stakelink/s/990
---
## CTF
| CTF | Flag Captured | Provider |
| --- | ------------- | -------- |
| A-Maze-X secureum‬ | [SecureVault](https://github.com/eshumanohare/secureum-a-maze-x-challenges/blob/main/test/N1-SecureVault-easy.js), [Weirdo-easy](https://github.com/eshumanohare/secureum-a-maze-x-challenges/blob/main/test/N2-Weirdo-easy.js), [TimeLock-easy](https://github.com/eshumanohare/secureum-a-maze-x-challenges/blob/main/test/N3-TimeLock-easy.js), [Padlock-medium](https://github.com/eshumanohare/secureum-a-maze-x-challenges/blob/main/test/N4-Padlock-medium.js), [BecomeMaster-medium](https://github.com/eshumanohare/secureum-a-maze-x-challenges/blob/main/test/N5-BecomeMaster-medium.js) | Secureum
| Secureum A-MAZE-X Stanford | [Challenge0](https://github.com/eshumanohare/DeFi-Security-Summit-Stanford/blob/foundry/test/Challenge0.t.sol), [Challenge1](https://github.com/eshumanohare/DeFi-Security-Summit-Stanford/blob/foundry/test/Challenge1.t.sol), [Challenge2](https://github.com/eshumanohare/DeFi-Security-Summit-Stanford/blob/foundry/test/Challenge2.t.sol), [Challenge3](https://github.com/eshumanohare/DeFi-Security-Summit-Stanford/blob/foundry/test/Challenge3.t.sol) | Secureum
---
## Blogs
| Title |
| ----- |
| [Rareskills Solidity Riddles Solutions in Foundry](https://coinsbench.com/rareskills-solidity-riddles-solutions-in-foundry-a5d093eb3b45) |
| [The vulnerable over-collateralised loan CTF](https://medium.com/coinsbench/the-vulnerable-over-collateralised-loan-ctf-0ef68b8f5118) |
