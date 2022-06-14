<div align="center"><img width="400" src="https://user-images.githubusercontent.com/32484870/169264834-35b0831e-c6fd-417e-9675-477424488c60.jpeg"></div>
<br/>

<div align="center"><a href="https://nested.fi" > https://nested.fi </a></div>

# Nested contest details

-   $33,250 USDC main award pot
-   $1,750 USDC gas optimization award pot
-   Join [C4 Discord](https://discord.gg/code4rena) to register
-   Submit findings [using the C4 form](https://code4rena.com/contests/2022-06-nested-contest/submit)
-   [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
-   Starts June 15, 2022 20:00 UTC
-   Ends June 18, 2022 19:59 UTC

## Scope 

**TOTAL = 1733 LOC & 18 Contracts**

> In this README you can find references to smart contracts that **are not part of the scope** (_StakeDAO operator_ for exemple), these contracts are mentioned because it is important to understand them to have a better view of how the protocol works in general.

### Core scope

| Contract name                     | Github URL                                                                                                                          | LoC |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | --: |
| NestedFactory                     | [NestedFactory.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/NestedFactory.sol)                             | 452 |
| OperatorResolver                  | [OperatorResolver.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/OperatorResolver.sol)                       |  59 |
| Withdrawer                        | [Withdrawer.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/Withdrawer.sol)                                   |  18 |
| /abstracts/MixinOperatorResolver  | [MixinOperatorResolver.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/abstracts/MixinOperatorResolver.sol)   |  68 |
| /abstracts/OwnableProxyDelegation | [OwnableProxyDelegation.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/abstracts/OwnableProxyDelegation.sol) |  35 |
| /libraries/ExchangeHelpers        | [ExchangeHelpers.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/libraries/ExchangeHelpers.sol)               |  21 |

### Operator scope

| Contract name                                      | Github URL                                                                                                                                                   | LoC |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | --: |
| /operators/Beefy/BeefyVaultOperator                | [BeefyVaultOperator.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Beefy/BeefyVaultOperator.sol)                            |  62 |
| /operators/Beefy/BeefyVaultStorage                 | [BeefyVaultStorage.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Beefy/BeefyVaultStorage.sol)                              |  20 |
| /operators/Beefy/lp/BeefyZapBiswapLPVaultOperator  | [BeefyZapBiswapLPVaultOperator.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Beefy/lp/BeefyZapBiswapLPVaultOperator.sol)   | 167 |
| /operators/Beefy/lp/BeefyZapUniswapLPVaultOperator | [BeefyZapUniswapLPVaultOperator.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Beefy/lp/BeefyZapUniswapLPVaultOperator.sol) | 166 |
| /operators/Paraswap/ParaswapOperator               | [ParaswapOperator.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Paraswap/ParaswapOperator.sol)                             |  35 |
| /operators/Yearn/YearnCurveVaultOperator           | [YearnCurveVaultOperator.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Yearn/YearnCurveVaultOperator.sol)                  | 176 |
| /operators/Yearn/YearnVaultStorage                 | [YearnVaultStorage.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/operators/Yearn/YearnVaultStorage.sol)                              |  26 |
| /libraries/CurveHelpers                            | [CurveHelpers.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/libraries/CurveHelpers/CurveHelpers.sol)                                 |  60 |
| /libraries/StakingLPVaultHelpers                   | [StakingLPVaultHelpers.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/libraries/StakingLPVaultHelpers.sol)                            |  92 |


### Governance scope

| Contract name                           | Github URL                                                                                                                                     | LoC |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | --: |
| /governance/OwnerProxy                  | [OwnerProxy.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/governance/OwnerProxy.sol)                                   |  19 |
| /governance/TimelockControllerEmergency | [TimelockControllerEmergency.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/governance/TimelockControllerEmergency.sol) | 186 |
| /governance/scripts/OperatorScripts     | [OperatorScripts.sol](https://github.com/code-423n4/2022-06-nested/blob/main/contracts/governance/scripts/OperatorScripts.sol)                 |  71 |

## Previous Audits

The preview version has been audited 4 times (from oldest to newest):

-   [Peckshield Audit Report v1.0](audits/PeckShield-Audit-Report-Nested-v1.0.pdf)
-   [Red4Sec Audit Report v1.0](audits/Red4Sec_Nested_Finance_Security_Audit_Report_v3.pdf)
-   [CodeArena 2021-11](https://code4rena.com/reports/2021-11-nested)
-   [CodeArena 2022-02](https://code4rena.com/reports/2022-02-nested)

⚠️ **All issues already surfaced in the [previous audit](https://code4rena.com/reports/2022-02-nested) will be "invalid"**.

## New version

This new version includes the corrections of the previous audits and new features.

### Fixes from [last audit](https://github.com/code-423n4/2022-02-nested)
- **[QA Report fixes#99](https://github.com/NestedFi/nested-core-lego/pull/99)**
    - QA Report [code-423n4/2022-02-nested-findings#4](https://github.com/code-423n4/2022-02-nested-findings/issues/4)
    - QA Report [code-423n4/2022-02-nested-findings#9](https://github.com/code-423n4/2022-02-nested-findings/issues/9)
    - QA Report [code-423n4/2022-02-nested-findings#24](https://github.com/code-423n4/2022-02-nested-findings/issues/24)
    - QA Report [code-423n4/2022-02-nested-findings#40](https://github.com/code-423n4/2022-02-nested-findings/issues/40)
    - QA Report [code-423n4/2022-02-nested-findings#45](https://github.com/code-423n4/2022-02-nested-findings/issues/45)
    - QA Report [code-423n4/2022-02-nested-findings#49](https://github.com/code-423n4/2022-02-nested-findings/issues/49)
    - QA Report [code-423n4/2022-02-nested-findings#50](https://github.com/code-423n4/2022-02-nested-findings/issues/50)
    - QA Report [code-423n4/2022-02-nested-findings#52](https://github.com/code-423n4/2022-02-nested-findings/issues/52)
    - QA Report [code-423n4/2022-02-nested-findings#65](https://github.com/code-423n4/2022-02-nested-findings/issues/65)
    - QA Report [code-423n4/2022-02-nested-findings#70](https://github.com/code-423n4/2022-02-nested-findings/issues/70)
- **[Gas optimizations fixes#101](https://github.com/NestedFi/nested-core-lego/pull/101)**
    - Gas Optimizations [code-423n4/2022-02-nested-findings#72](https://github.com/code-423n4/2022-02-nested-findings/issues/72) ([f2fb697](https://github.com/NestedFi/nested-core-lego/commit/f2fb6974e0f471c027e7b2ed59c33f1052af54af))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#68](https://github.com/code-423n4/2022-02-nested-findings/issues/68) ([4c752b1](https://github.com/NestedFi/nested-core-lego/commit/4c752b16d8b76ce1e4e8779ba915f9e325d24ee5))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#67](https://github.com/code-423n4/2022-02-nested-findings/issues/67) ([5d75f4c](https://github.com/NestedFi/nested-core-lego/commit/5d75f4c620c7d11eab2507f85f204a97cfb3de36))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#57](https://github.com/code-423n4/2022-02-nested-findings/issues/57) ([f72f8e5](https://github.com/NestedFi/nested-core-lego/commit/f72f8e5137ab2bf2d1a4a0c8665dc9f1528fd37c))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#56](https://github.com/code-423n4/2022-02-nested-findings/issues/56) ([250bca4](https://github.com/NestedFi/nested-core-lego/commit/250bca42480a9a3282dcd4641a48b456f01d82a6))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#55](https://github.com/code-423n4/2022-02-nested-findings/issues/55) ([ca9b7fd](https://github.com/NestedFi/nested-core-lego/commit/ca9b7fd57c4758240cba842eceb135a0866deeb2))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#39](https://github.com/code-423n4/2022-02-nested-findings/issues/39) ([5cebd50](https://github.com/NestedFi/nested-core-lego/commit/5cebd505c29a0986c1311dc7d80c80b8a567e62a))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#32](https://github.com/code-423n4/2022-02-nested-findings/issues/32) ([835fb74](https://github.com/NestedFi/nested-core-lego/commit/835fb7451fe15b986513e2522c455e8ddb97d830))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#8](https://github.com/code-423n4/2022-02-nested-findings/issues/8)   ([51ccc99](https://github.com/NestedFi/nested-core-lego/commit/51ccc99a661a7e70335e189a430dfae0a0437988))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#5](https://github.com/code-423n4/2022-02-nested-findings/issues/5)   ([2a82425](https://github.com/NestedFi/nested-core-lego/commit/2a8242533aaced160f8c1b6d1fd617aca489eefb))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#28](https://github.com/code-423n4/2022-02-nested-findings/issues/28) ([33ab760](https://github.com/NestedFi/nested-core-lego/commit/33ab760e1600d5e10e0c4c968c18cb249f126c73))
- **[Med/High Risk fixes#100](https://github.com/NestedFi/nested-core-lego/pull/100)**
    - Undesired behavior [code-423n4/2022-02-nested-findings#6](https://github.com/code-423n4/2022-02-nested-findings/issues/6) ([0c71774](https://github.com/NestedFi/nested-core-lego/commit/0c717742a11fa31f6e8f9ef83545fc43b37e91d8))
    - Royalty owner can steal Stakeholders fees [code-423n4/2022-02-nested-findings#10](https://github.com/code-423n4/2022-02-nested-findings/issues/10) ([e82319e](https://github.com/NestedFi/nested-core-lego/commit/e82319e36f32cb8b500c9b732d2b9669a21c0982))
    - Gas Optimizations [code-423n4/2022-02-nested-findings#15](https://github.com/code-423n4/2022-02-nested-findings/issues/15) ([da9a817](https://github.com/NestedFi/nested-core-lego/commit/da9a817ad3f540f2f11724b265edebc03d1360a3))
    - Wrong logic around areOperatorsImported [code-423n4/2022-02-nested-findings#17](https://github.com/code-423n4/2022-02-nested-findings/issues/17) ([720b450](https://github.com/NestedFi/nested-core-lego/commit/720b4502ca781be8575a131b1db6d98d0bf97629))
    - Wrong rebuild cache logic [code-423n4/2022-02-nested-findings#18](https://github.com/code-423n4/2022-02-nested-findings/issues/18) ([d2e48a8](https://github.com/NestedFi/nested-core-lego/commit/d2e48a8950659bd176257df26e346bb87a774bc3))
    - Destroy can avoid the bulk of fees [code-423n4/2022-02-nested-findings#27](https://github.com/code-423n4/2022-02-nested-findings/issues/27) ([2ab7934](https://github.com/NestedFi/nested-core-lego/commit/2ab79340b2ad21eaf74d6549a4bb7837e3379fd9))
    - NestedFactory does not track operators properly [code-423n4/2022-02-nested-findings#38](https://github.com/code-423n4/2022-02-nested-findings/issues/38) ([1a16a51](https://github.com/NestedFi/nested-core-lego/commit/1a16a5104bdd3cc4fed320deba9d1d6ab6d630c2))
    - NestedFactory: User can utilise accidentally sent ETH funds via processOutputOrders() / processInputAndOutputOrders() [code-423n4/2022-02-nested-findings#44](https://github.com/code-423n4/2022-02-nested-findings/issues/44) ([ac472b4](https://github.com/NestedFi/nested-core-lego/commit/ac472b425cda9e53a130ecd0149657bdc3ce2481))

### Ownership architecture [(see more)](#ownership--governance)

_**Pull request:**_ [feat: OwnerProxy #116](https://github.com/NestedFi/nested-core-lego/pull/116)
In order to complete the ownership architecture, we need the OwnerProxy contract in charge of executing scripts for the Timelock (run transactions atomically).

### Operators

#### Beefy Single asset vault

_**Pull request:**_ [[New Operator] - Beefy Single Asset Vault #107](https://github.com/NestedFi/nested-core-lego/pull/107)
New operator to deposit/withdraw in [**Beefy single asset vaults**](https://app.beefy.finance/)
This operatorcan be deployed on every chains where Beefy is available.

#### Beefy LP vault

_**Pull request:**_ [[New Operator] - Beefy LP Vault #114](https://github.com/NestedFi/nested-core-lego/pull/114)
New operator to deposit/withdraw in [**Beefy LP asset vaults**](https://app.beefy.finance/)
This operatorcan be deployed on every chains where Beefy is available.

#### Paraswap

_**Pull request:**_ [[New Operator] - Paraswap #109](https://github.com/NestedFi/nested-core-lego/pull/109)
New operator to swap tokens in [Paraswap](https://app.paraswap.io/)
This operatorcan be deployed on every chains where [Paraswap](https://app.paraswap.io/) is available.

#### Yearn Curve vaults

_**Pull request:**_ [[New Operator] StakeDAO + Yearn (curve pools) #119](https://github.com/NestedFi/nested-core-lego/pull/119)
New operator to deposit/withdraw in [Yearn](https://yearn.finance/#/vaults) vaults that use [Curve](https://curve.fi/) managed assets.
This operatorcan be deployed on every chains where [Yearn](https://yearn.finance/#/vaults) has Curve vault available.

> **NOTE**: This operator is almost identical to the **StakeDAO operator**, so we have only included the Yearn operator in the audit scope and not the StakeDAO one.
> We factorized the code of these two operators in the libraries `StakingLPVaultHelpers.sol` and `CurveHelpers.sol`.

### Entry/exit fees management

_**Pull request:**_ [feat: Upgradeable Fees #113](https://github.com/NestedFi/nested-core-lego/pull/113)
We had introduced upgradeability of fees and the notion of "EntryFees/ExitFees" (new values) :

-   `EntryFees` : Applied when funds stay inside of the portfolio.
-   `ExitFees` : Applied when funds are withdrawed from the portfolio.

### Nested asset tokenURI mechanism

_**Pull request:**_ [feat: Update tokenURI mechanism #103](https://github.com/NestedFi/nested-core-lego/pull/103)
We updated the mechanism to set the tokenURI:

-   Remove mintWithMetadata and backfillTokenURI (with the \_tokenURIs map).
-   Add reveal/unrevealed URI
-   Add contract URI

## Known issues/topics

### Copy my portfolio (fees trick)

A user can copy his own portfolio to reduce the fees. However, a require statement will not fix this issue.

This problem cannot be corrected but only mitigated, since the user can use two different wallets.
Currently the front-end doesn’t allow to duplicate a portfolio with the same address.

### Deflationary, Rebase and exotic Tokens

The protocol is not fully compatible with deflationary/rebase tokens. In fact, you can add a deflationary/rebase token to your portfolio but
it can lead to unpredictable behaviors (positive or negative).
We have chosen to manage the tokens with a fixed amount (the input) after considering several solutions.

There are also tokens that have exotic implementations that will not handle to avoid unpredictable behaviors, or bypass protocol operations.

**So, how can we mitigate that ?**

We are maintaining a list of all rebase tokens (source coingecko, which is well maintained), but also exotic tokens and prevent users from adding them to their portfolio on the platform.

### Low decimals and Fees calculation

We can encounter tokens with different decimals and sometimes 0 decimals. This is the case with [MPS](https://etherscan.io/token/0x96c645D3D3706f793Ef52C19bBACe441900eD47D#readContract). It can be problematic as we can loose precision when calculating fees.

### Miscellaneous already surfaced

| Issue                                                                                         | Github URL                                                               |                                                                                                    Comment |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------: |
| `TransferOwnership` should be a two step process                                              | [link](https://github.com/code-423n4/2021-11-nested-findings/issues/101) |                                                                                                            |
| `NestedAsset`: `mintWithMetadata` and `backfillTokenURI` are not used                         | [link](https://github.com/code-423n4/2021-11-nested-findings/issues/179) | We assume that the next factory might use these functions. Therefore we want to keep this unused function. |
| Accidentally calling `withdraw` twice with the same parameters could withdraw multiple assets | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/33)  |                                                It is a front end and not really related to smart contract. |
| Unbounded number of shareholders can cause DOS                                                | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/2)   |                                                                                                            |

### Gas optimizations already surfaced

| Issue                                                                                                                               | Github URL                                                              |                                                                                                                   Comment |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------: |
| Use of constant keccak variables results in extra hashing                                                                           | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/71) |                                                                                                                           |
| Use custom errors instead of the revert strings                                                                                     | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/63) |                                                                                                                           |
| Change the incremental logic from `i++` to `++i`                                                                                    | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/16) |                                                                                                                           |
| An array’s length should be cached in for-loops                                                                                     | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/28) |                                                                                           When the array will no be large |
| Consider introducing an upper limit for `_timestamp` in updateLockTimestamp                                                         | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/66) |                                                                               We are not sure about an upper limit to set |
| There is no limit on how many operator that can be added                                                                            | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/58) |                                                                                                                           |
| Remove unused `ETH` variable from `FeeSplitter`                                                                                     | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/46) | We don't know if we will remove this variable,It can be very useful to migrate funds (if needed, not used for the moment) |
| Functions that add or remove `operators` or `shareholders` iterate over a whole array, consider using `EnumerableSet` to store them | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/67) |                                                                                                                           |
| Function `withdraw` in `NestedFactory` calls `nestedRecords` twice                                                                  | [link](https://github.com/code-423n4/2022-02-nested-findings/issues/67) |                                                                                                                           |

## Coverage

Run `npx hardhat coverage` to run test and generate the coverage summary.

> When you run `npx hardhat coverage`, test will be ran with the context you specified in the [.env configuration](https://github.com/NestedFi/nested-core-lego#testing).
> Only tests that can be run in the environment you have configured will be run to generate the coverage summary.

> To get the total coverage, it is necessary to run `npx hardhat coverage` with all the existing configurations, to reach all the written tests.

> You can find the 3 existing configrations (BSC, ETH and without fork) in [.env.exemple](https://github.com/NestedFi/nested-core-lego/blob/master/.env.example) file.

### Coverage ran without fork

#### Global coverage - tested without fork

> The missing coverage is tested in the [BSC fork context](#coverage-ran-in-bsc-fork-context) or the [ETH fork context](#coverage-ran-in-eth-fork-context)

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/without-fork-1.png"></div>

#### Main contracts - tested without fork

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/without-fork-2.png"></div>

### Coverage ran in ETH fork context

#### Libraries - tested on ETH fork

> The rest of the coverage is in the BSC fork coverage context under [Libraries - tested on BSC fork](#libraries---tested-on-bsc-fork).

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/eth-2.png"></div>

#### CurveHelpers - tested on ETH fork

> The rest of the coverage is in the BSC fork coverage context under [CurveHelpers - tested on BSC fork](#curvehelpers---tested-on-bsc-fork).

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/eth-3.png"></div>

#### Yearn curve vault operator

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/eth-4.png"></div>

### Coverage ran in BSC fork context

#### Libraries - tested on BSC fork

> The rest of the coverage is in the ETH fork coverage context under [Libraries - tested on ETH fork](#libraries---tested-on-eth-fork).

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/bsc-2.png"></div>

#### CurveHelpers - tested on BSC fork

> The rest of the coverage is in the ETH fork coverage context under [CurveHelpers - tested on ETH fork](#curvehelpers---tested-on-eth-fork).

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/bsc-3.png"></div>

#### Beefy operators

<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/bsc-5.png"></div>
<div align="left"><img style="width:100%; max-width: 1000px" src="/static/coverage-screenshots/bsc-6.png"></div>

## Links

-   **Website** : https://nested.fi
-   **Documentation** : https://docs.nested.fi/
-   **Medium** : https://medium.com/@nestedfi
-   **Github** : https://github.com/NestedFi
-   **Twitter** : https://twitter.com/NestedFi
-   **Telegram** : https://t.me/NestedFinanceChannel
-   **Discord** : https://discord.gg/VW8ZZsACzd

## Contact us 📝

Wardens! If you have any questions, please contact us!

#### Axxe (Smart contract engineer)

-   **Telegram** : @axxedev
-   **Discord** : axxe#8561
-   **Schedule a call** : [Calendly](https://calendly.com/maxime-brugel/lets-talk)

#### Adrien (CTO)

-   **Telegram** : @adrienspt
-   **Discord** : Adrien | Nested Finance#6564
-   **Schedule a call** : [Calendly](https://calendly.com/adrien-supizet/30min)

## Try the application

If you want to try Nested, go to : https://app.nested.fi/.

It can help to better understand the protocol context.

---

# Introduction

Nested is a decentralized protocol providing customizable financial products in the form of NFTs.
The platform allows users to put several digital assets, i.e. ERC20 tokens, inside an NFT (abbreviated as `NestedNFT`).
<br/>

Each NestedNFT is backed by underlying assets:

-   Purchased or sold on a decentralized exchange (AMM).
-   Collected/earned after adding liquidity or staking.
-   Exchanged/Minted on a protocol that is not a decentralized exchange.
-   (...)

The main idea is to allow adding modules (**operators**) to interact with new protocols
and enable new assets, without re-deploying.

> The tokens are stored on a self-custodian smart contract.

At the end of the creation process, the user receives the NFT which allows to control all underlying assets of the portfolio.
Furthermore, we allow users to copy other users NestedNFTs. The creator of the initial NestedNFT earns royalties.

### _Further documentation and details can be found here: https://docs.nested.finance/_

# Architecture

![image](https://user-images.githubusercontent.com/22816913/152804262-e8879475-8873-43a9-9a53-18da1517b3fd.png)

## Core contracts

| Name                | Purpose                                                                                                                    |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **NestedFactory**   | Entry point to the protocol. Holds the business logic. Responsible for interactions with operators (submit orders).        |
| **NestedAsset**     | Collection of ERC721 tokens. Called NestedNFT across the codebase.                                                         |
| **NestedReserve**   | Holds funds for the user. Transferred from the NestedFactory.                                                              |
| **NestedRecords**   | Tracks underlying assets of NestedNFTs. (Amount, NestedReserve).                                                           |
| **FeeSplitter**     | Receives payments in ERC20 tokens from the factory when fees are sent. Allows each party to claim the amount they are due. |
| **NestedBuyBacker** | Pulls tokens from the FeeSplitter, buys back NST tokens on the market, and burns a part of it.                             |

## Upgradability

The contracts `NestedAsset`, `NestedReserve`, and `NestedRecords` are whitelisting multiple factories (to create NFTs, update records, withdraw from reserve,...).

However, we are also using the [TransparentUpgradeableProxy](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/proxy/transparent/TransparentUpgradeableProxy.sol) for `NestedFactory`. Then, the users doesn't have to approve multiple times.

We have kept both mechanisms to get the best flexibility.

## Lock

The users can lock their NFTs until a certain date (timestamp) by calling `updateLockTimestamp`. This feature allows the "hold by design".

## Operators (modularization)

### What is an operator?

`NestedFactory` is the main smart contract, but it can't work without the Operators.

As mentioned in the introduction, we designed the protocol to be **modular**.
We want to be able to interact with any protocol in exchange for an ERC20 token.

So, we had to deal with two issues :

-   How to interact with 5, 10, or 20 protocols without blowing up the bytecode size and having too much logic?
-   How to add new interactions without redeploying the `NestedFactory` contract?

Our solution is called the "**Operator**"... A new interaction is a new operator and can be added on the fly.
They kind of work like [libraries](https://docs.soliditylang.org/en/v0.8.9/contracts.html#libraries), but since we don't want to redeploy the factory,
they are contracts that are called via `delegatecall` and referenced by the `OperatorResolver`.

### Operator Resolver

An operator allows performing a precise action, like _"swap my token A for a token B"_ with a specific function, but the operator/interface will change depending on the action/context. To interact with new operators on the fly, we must expose new interfaces to the Factory.
The `OperatorResolver` will whitelist all the Operator (`address`) with the selectors (`bytes4`) since we can't trust the caller to provide these informations.

```javascript
struct Operator {
    address implementation;
    bytes4 selector;
}
```

The caller will send the (imported) `bytes32` name of the Operator/Function, for example "ZeroEx::performSwap".

The `OperatorResolver` will return the `address` + `selector` if the call is whitelisted and revert if not.

### Storage

Since the operators are called via `delegatecall`: _how can we store/retrieve useful data?_
<br>In fact, we cannot trust the Factory to provide all the data, like the address of the protocol. It must be stored and managed by the owner.

When deploying an operator, it will also deploy the storage contract and transfer the ownership to `msgSender()`.

### Diagram

![image](https://user-images.githubusercontent.com/22816913/152804758-98de74eb-e09c-44ac-8504-32b40c3624ae.png)

### Contracts

| Name                           | Purpose                                                                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| OperatorResolver               | Allows the factory to identify which operator to interact with.                                                          |
| MixinOperatorResolver          | Abstract contract to load authorized operators in cache.                                                                 |
| ZeroExOperator                 | Performs token swaps through 0x ([read more](contracts/operators/ZeroEx/README.md)).                                     |
| ZeroExStorage                  | ZeroExOperator storage contract. Must store the 0x `swapTarget`.                                                         |
| FlatOperator                   | Handles deposits and withdraws. No interaction with any third parties ([read more](contracts/operators/Flat/README.md)). |
| BeefyVaultOperator             | Handles deposits and withdraws in a Beefy single vault (native or non-native).                                           |
| BeefyZapBiswapLPVaultOperator  | Handles deposits and withdraws in a Beefy Biswap LP vault using zapper.                                                  |
| BeefyZapUniswapLPVaultOperator | Handles deposits and withdraws in a Beefy UniswapV2 LP vault using zapper.                                               |
| BeefyVaultStorage              | Handles whitelisting of Beefy Vault or Zapper.                                                                           |
| ParaswapOperator               | Performs token swaps through Paraswap.                                                                                   |

_More operators will be added. e.g. CurveOperator or SynthetixOperator_

### Orders

The `NestedFactory` is using the operators to interact with other protocols. The call from the Factory to an Operator is an "Order".

An Order has several information:

-   The operator/selector to use
-   The token processed (swapped, stacked,...) by the operator (from the portfolio or wallet).
-   The calldatas (without the selector).

```javascript
struct Order {
    bytes32 operator;
    address token;
    bytes callData;
}
```

It helps us to make **one** interaction, but we want to make multiple interactions. For example, to create a portfolio with multiple tokens, we need to "batch" these orders.

**There are two types of "Batched Orders" processed by the Factory to create or edit Portfolios :**

#### Batched Input Orders

<div align="center"><img src="./static/input-orders.png" width="650"></div>

-   One same input for every orders but multiple outputs.
-   0.3% fee on the input.
-   The input (_source_) is from a wallet **or** a porfolio owned by the transactions signer.
-   The ouput (_destination_) is the portfolio owned by the transactions signer (**only**).

```javascript
struct BatchedInputOrders {
    IERC20 inputToken;
    uint256 amount;
    Order[] orders;
    bool fromReserve;
}
```

#### Batched Output Orders

<div align="center"><img src="./static/output-orders.png" width="650"></div>

-   Multiple inputs for every orders but one output.
-   0.3% fee on the output if operation does not reduce TVL, 0.8% if it does.
-   The input (_source_) is the portfolio owned by the transactions signer (**only**).
-   The ouput (_destination_) is from a wallet **or** a portfolio owned by the transactions signer.

```javascript
struct BatchedOutputOrders {
    IERC20 outputToken;
    uint256[] amounts;
    Order[] orders;
    bool toReserve;
}
```

#### Example `processInputOrders` flow

<div align="center"><img src="./static/processInputOrders.png" width="1200"></div>

## Nested Factory interaction with the Nested Reserve and Nested Records

The Nested Reserve stores underlying assets of all NestedNFTs. The Nested Records keeps track of which underlying assets are associated with a specific NestedNFT.
Hence, each time the Nested Factory needs to interact with user funds (which are represented as a NestedNFT), it will first check the balance of tokens associated with the NestedNFT through Nested Records. If needed, it will then transfert funds to the Nested Reserve or withdraw funds from it.

## Native Token Management

The Nested protocol only handles ERC20 when calling operators.  
If the msg.sender is not the withdrawer, the sent ETH used to feed a portfolio are automatically converted to WETH when received.

### WETH Conversion

The conversion from ETH to WETH is done when submitting an order through `_submitInOrders` or `_submitOutOrders`.

Before submitting orders, the NestedFactory transfers the input tokens from the NestedReserve (or the msg.sender) to the factory and converts the sent ETH to WETH.

### Use of ETH in operators

There are some operators who use ETH directly and not WETH.  
In this case, the operator uses the Withdrawer to get the ETH back from the WETH contract before using it.

> Only the Withdrawer can send ETH to the NestedFactory without automatic WETH conversion.

## Royalties

Royalties are a part of the fee collected by the protocol and they are collected during every step of a copied portfolio lifecycle (copy, update, deposit, withdraw).

### Fees distribution

For now, the fees are shared equally between portfolio creators (as royalties) and Nested.

**First scenario:** When a portfolio is created from scratch, all fees go to Nested Finance Ltd and there are no royalties.<br/>
**Second scenario:** When a portfolio is replicated, the fees are shared equally between Nested Finance Ltd. and the original creator of the Nested portfolio.

This distribution is done in the `feeSplitter.sol` with the ratio between the `royaltiesWeight` and the `shareholders` weights.
Currently, we have `royaltiesWeight = 50` and **one** shareholder (_Nested_) with `weight = 50`.

> **totalWeights** always equals **royaltiesWeight** + all shareholders **weights**

# Ownership & Governance

Some functions of the protocol require admin rights (`onlyOwner` using `Ownable` from [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol)). Same with the [TransparentUpgradeableProxy](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/proxy/transparent/TransparentUpgradeableProxy.sol) which need an **Admin**.

<img width="1011" alt="image" src="./static/ownership.png">

The contracts are owned by the `OwnerProxy` which is a [DSProxy](https://github.com/dapphub/ds-proxy) fork without a cache, where only the Timelock can execute the scripts.

The TimelockControllerEmergency is a [TimelockController](https://docs.openzeppelin.com/contracts/4.x/api/governance#TimelockController) fork.
It introduces the "Emergency Role" to execute a transaction in an instantaneous way.
Only the "Emergency Multisig" has this role, with 5 members and 5 approvals needed (in the case of an urgent fix).
On the other hand, the "Operational Multisig" can schedule/execute transactions with a **6-hours** delay, with 3 members and 2 approvals needed.

# Development & Testing

## Setup

-   Install Node > 12
-   Install Yarn
-   Run `yarn install`
-   Run `cp .env.example .env`
-   Insert a dummy mnemonic and a mainnet api key in the `.env` file

### Run tests

Tests can be run without fork, with a BSC fork or with an ETH fork by running `yarn test`.
You can configure how to run the tests by configuring your `.env` file as follow:

-   To run the tests **without fork**:

```bash
FORKING="false"
```

-   To run the tests **with BSC fork**:

```bash
FORKING="true"
FORK_CHAINID="56"
FORK_URL="https://bsc-dataseed.binance.org/"
```

-   To run the tests **with BSC fork**:

```bash
FORKING="true"
FORK_CHAINID="1"
FORK_URL="<YOUR_ETH_RPC_ENDPOINT_URL>"
```

## Commands

-   Start a local blockchain
    `yarn run`

-   Start a hardhat console
    `yarn console`

-   Compile
    `yarn compile`

-   Generate typechain files
    `yarn typechain`

-   Run tests
    `yarn test`

# License

[GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.html)
