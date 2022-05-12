---
description: Learn more about the WONE bank and how it exactly works.
---

# WONE Bank

## The Hermes WONE Bank

![](<../.gitbook/assets/WONE Bank.png>)

{% hint style="info" %}
This content was contained within [#the-new-hermes-wone-bank](../the-hermes-protocol/plts-to-hrms-transition.md#the-new-hermes-wone-bank "mention"), but is being highlighted here for maximum visibility.
{% endhint %}

To bridge the gap between the end of farming emissions (new PLTS being minted) and the beginning of the swap period, we have developed a new bank contract. This **WONE Bank** allows users to deposit WONE to obtain the remaining 500,000 PLTS stored in the treasury.&#x20;

{% hint style="warning" %}
**Critically, the deposited WONE will be used to create HRMS/WONE LP tokens at the moment of liquidity addition. You will receive HRMS/WONE LP and not WONE when this bank unlocks.**
{% endhint %}

The PLTS obtained from the WONE Bank can be deposited in the public swap contract to obtain more pHERMES. This will allow investors to obtain about **16% of the PLTS supply.**

{% hint style="info" %}
To look more at the math behind this contract and estimated APRs, you can view this [google sheet](https://docs.google.com/spreadsheets/d/1mVKGZvjQubqxeaCxpBVMVaDMDoCVSEN8/edit#gid=1817589439).&#x20;
{% endhint %}

### WONE Bank Rewards:&#x20;

* PLTS rewards **start on block 24,095,140** (\~15 Mar 2022 2:28:25 AM EST) and **end on block 26,376,387 (\~May 7th).**
* PLTS that can be sold or exchanged for pHERMES.&#x20;
* 100% of deposited WONE will be converted to Hermes DEX HRMS/WONE LP. (50% buys HRMS and is paired with the remaining 50% WONE). You will withdraw HRMS/WONE LP tokens and be able to farm with them at the same moment (when the DEX launches)!

### Contract functionality:

The operation of the contract will be as follows:

1. User deposits WONE.&#x20;
2. User receives a token share that will mark the proportional amount of LP.&#x20;
3. User can harvest their PLTS rewards at any time.&#x20;
4. PLTS rewards are stopped around 1 day before adding liquidity to HRMS/WONE.&#x20;
5. Investors swap their PLTS to pHRMS.&#x20;
6. HRMS/ONE liquidity is added in the **SAME TRANSACTION** that the WONE bank swaps half of the deposited WONE to HRMS. The exact block of this call is not defined. When this function is called, the contract performs the following:
   * Contract Admin initiates initial HRMS/ONE liquidity ($150,000 in WONE + 400,000 HRMS) using the Hermes Router.
   * The Bank Contract purchases HRMS with 50% of the bank's WONE value.&#x20;
   * The Bank Contract creates HRMS/WONE LP with remaining 50% in WONE and the received HRMS. This LP is now fully unlocked and able to be withdrawn by users.
   * Users will return their 'Bank Share' tokens to claim their proportional share of new Hermes $WONE / $HRMS LP. They are free to do whatever they wish with this LP
   * We will utilize a single block to execute these transactions, avoiding manual errors by the team, external bots that vary the launch price before the bank's WONE purchase is made, and **never** have direct access to the WONE deposited by users.&#x20;
7. The user, once liquidity is added, can access their LP corresponding to 100% of their deposited value plus the fees generated so far (due to the shared token format). From there they may split their LP (take profit) or deposit it in the farm and generate yield.

{% hint style="info" %}
Mainnet contract address: 0xa19765e275669c1162b099c7c8553c23b779cd83

Example Testnet AdminSwap call (note, uses Viper router but no functional difference when using Hermes router on mainnet): [https://explorer.testnet.harmony.one/tx/0x7df5161126137a77a6a160eb1ab7a9c7ac9e75051fa30bfb82f708c326a751e1](https://explorer.testnet.harmony.one/tx/0x7df5161126137a77a6a160eb1ab7a9c7ac9e75051fa30bfb82f708c326a751e1)

Github: [https://github.com/Hermes-defi/plts-special-bank](https://github.com/Hermes-defi/plts-special-bank)
{% endhint %}
