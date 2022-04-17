---
description: Auto-compounding and fully trustless liquid ONE Staking.
---

# hONE

## hONE (Hermes Staked ONE)<img src="../.gitbook/assets/Hermes Staked ONE.png" alt="" data-size="line">

hONE is a defi primitive designed to unlock illiquid ONE held within validators on the Harmony Blockchain. It utilizes staking precompiles made available through a hard fork in the Harmony Blockchain in February to directly interact with Harmony validators, meaning your funds are only accessible through your wallet. &#x20;

### hONE Mechanisms

The mechanisms (and code underlying this contract) are open-source and available on the [Hermes GitHub](https://github.com/Hermes-defi/hermes-hone-multi). Briefly, the user deposits ONE into the hONE contract which mints hONE and deposits the ONE into an eligible Validator. Users are then free to utilize their hONE in liquidity positions, farming liquidity-based yields as well as realize auto-compounding rewards from staking ONE to secure the Harmony blockchain.

When someone wishes to unstake hONE, there are two different options. First, the user can unstake hONE by depositing it back into the hONE contract and waiting 127 hours (or 7 epochs) to withdraw their undelegated ONE from the contract. Alternatively, they may sell their hONE for ONE through a DEX swap, which typically results in slightly less value for the premium of immediate access.&#x20;

### FAQ:

* _Are there fees associated with hONE?_
  * There are no additional fees planned for hONE, however, the Validators fee (typically 5%) are removed from rewards automatically.
* _When will I be able to use hONE?_ 🐰
  * hONE is currently under audit from Certik. Due to the nature of this contract, it may take additional time to audit fully. The expected date to receive an audit report is late May or early June.
* _Where will I be able to use hONE?_
  * Our initial focus for hONE will first be to establish hONE/ONE liquidity on Hermes. Once that reaches sufficient levels, hONE may start to be phased in as the WONE replacement on some of our farms.
  * Anyone is free to host hONE liquidity and utilize hONE outside of The Hermes Protocol, but likely this will be the place of its greatest adoption.
* _How does this differ from stONE?_
  * Hermes Staked ONE is unique in the fact that it operates in a fully trustless manner. Your ONE tokens are directly staked through the contract and there are no intermediaries with access to funds, not even contract admins.
  * Hermes Staked ONE does not have an additional 10% fee on staking rewards.
  * Hermes Staked ONE has open-source code and verified contracts.
  * Hermes Staked ONE will seek to help decentralize the Harmony Validator network, actively focusing on bringing unelected validators past the stable election threshold.
  * Hermes Staked ONE will enforce a reasonable maximum stake and undelegation value per transaction and will utilize a round-robin algorithm to undelegate from the Validator with the highest stake and delegate new deposits to the Validator with the lowest stake. It also implements a safe minimum threshold check to ensure undelegations would not result in a single validator falling below the election threshold.

