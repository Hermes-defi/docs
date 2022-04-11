---
description: All details relating to the PLTS to HRMS transition process.
---

# PLTS to HRMS Transition

## PLTS to HRMS Transition

Why is the PLTS to HRMS transition needed? PLTS has a hard-coded 3% transaction tax to fund our L2 Bank mechanism. Unfortunately, this makes it unsuitable for a DEX ecosystem and utility token. Because of this, we must transition PLTS to HRMS as well as migrate liquidity from ViperSwap to our own DEX.

The PLTS to HRMS transition has been our major focus for the past two to three weeks. We have reviewed, revised, given feedback, worked on spreadsheets until passing out, and debated all points of this process more times than we can count. We hope that this document can clearly answer all questions related to the transition process and the creation of HRMS. **This process is complicated with no perfect solution,** but we have created something we hope to be as user-friendly as possible.

Requirements:

* Extend PLTS rewards until the launch of Hermes Protocol
* Migrate PLTS held by users to Hermes (HRMS)
* Eliminate the PLTS token from circulation

Objectives to be met:&#x20;

* Incentivize all investors to switch their PLTS to HRMS
* Return as much value as possible through the transition
* Two simple routes to get HRMS: The PLTS swap or the WONE bank&#x20;
* Allow users to gain yield at all times (no gaps)&#x20;
* Migrate PLTS/DAI liquidity to HRMS/ONE liquidity&#x20;
* Easy user interaction across the entire process&#x20;
* Minimize price Impact and trading disruption&#x20;
* Creating solid tokenomics without compromising the future of HRMS

To accomplish these objectives, we will use the following mechanisms which are detailed extensively in the remainder of this document:&#x20;

* [PLTS Swap contract (Bank Boost) ](plts-to-hrms-transition.md#plts-swap-contract-bank-boost)
* [PLTS Swap contract (Public) ](plts-to-hrms-transition.md#plts-swap-contract-public)
* [WONE bank creation ](plts-to-hrms-transition.md#the-new-hermes-wone-bank)
* [HRMS liquidity added & WONE purchase ](plts-to-hrms-transition.md#point-of-liquidity-addition)
* [Redeem pHermes to HRMS contract (1:1)](plts-to-hrms-transition.md#what-is-phrms-and-why-are-we-using-it)
* [Transition of PLTS/DAI to HRMS/ONE](plts-to-hrms-transition.md#how-will-hermes-defi-handle-the-transition-from-plts-dai)

### PLTS Swap Contract (Bank Boost)

The Bank Boost swap contract will only be available to investors that deposited PLTS in the bank **before March 4th**. A snapshot at this time sums each addresses’ deposited PLTS across all banks and **allows them to swap with a bonus** for that amount of PLTS via a whitelist function. Only investors who have deposited in this contract **before this date** will be entitled to access the bonus rewards.

{% hint style="info" %}
Snapshot data:&#x20;

* Date and Time: March 4th 18.20pm GMT+1
* Total PLTS staked: 1,459,200.42 PLTS&#x20;
* price: $0.3653&#x20;
* Total PLTS value locked: $533.992,93
{% endhint %}

**This document shortly after this snapshot as a ‘stealth launch’ for the bonus.**

### PLTS Swap Contract (Public)

The public swap contract is available for all circulating PLTS that was not deposited into the bank before the snapshot. It will be available via an interface on our website.&#x20;

### PLTS to HRMS Swap Mechanisms

There will be two swap contracts, one for users who deposited their PLTS in the bank prior to the snapshot and a second one for all other PLTS. These two contracts will open and close at the same time.

In addition to the >$78,000 1DAI rewards paid to users who deposited PLTs into the bank, there will be a slightly more generous swap ratio compared to the public. Users who deposited before the snapshot will be able to swap **1PLTS to 0.66 pHRMS** (up to their maximum balance during the snapshot.&#x20;

All other PLTS (LP, held in wallets) will be able to swap 1 **PLTS for 0.56 pHRMS.**

| Bank Swap         | Public Swap       |
| ----------------- | ----------------- |
| 1 PLTS            | 1 PLTS            |
| 0.6610169492 HRMS | 0.5603998308 HRMS |

Users will deposit their PLTS in one or both of these contracts to receive pHERMES while the swap period is open (\~3 days). Two hours after the addition of HRMS/ONE liquidity on our new DEX, users will be able to exchange their pHERMES for HERMES at a 1:1 ratio.

To realize this swap, **6% of the total HRMS supply** will be used. **3.15%** will be used for bank investors and **2.85%** for public investors. For complete data please visit this link: [https://docs.google.com/spreadsheets/d/1mVKGZvjQubqxeaCxpBVMVaDMDoCVSEN8/edit#gid=1655498152 ](https://docs.google.com/spreadsheets/d/1mVKGZvjQubqxeaCxpBVMVaDMDoCVSEN8/edit#gid=1655498152)

### The NEW Hermes WONE Bank

To bridge the gap between the end of farming emissions (new PLTS being minted) and the beginning of the swap period, we have developed a new bank contract.

{% content-ref url="../hermes-products/wone-bank.md" %}
[wone-bank.md](../hermes-products/wone-bank.md)
{% endcontent-ref %}

This **WONE Bank** allows users to deposit WONE to obtain the remaining 500,000 PLTS stored in the treasury. **Critically, the deposited WONE will be used to create HRMS/WONE LP tokens at the moment of liquidity addition. You will receive HRMS/WONE LP and not WONE when this bank unlocks.**

The PLTS obtained from the WONE Bank can be deposited in the public swap contract to obtain more pHERMES. This will allow investors to obtain about **16% of the PLTS supply.**

{% hint style="info" %}
To look more at the math behind this contract and estimated APRs, you can view this google sheet. [https://docs.google.com/spreadsheets/d/1mVKGZvjQubqxeaCxpBVMVaDMDoCVSEN8/edit#gid=1817589439](https://docs.google.com/spreadsheets/d/1mVKGZvjQubqxeaCxpBVMVaDMDoCVSEN8/edit#gid=1817589439)
{% endhint %}

The rewards from the WONE bank are:&#x20;

* PLTS that can be sold or exchanged for pHERMES.&#x20;
* 100% of deposited WONE will be converted to Hermes DEX HRMS/WONE LP. (50% 'buys' HRMS and is paired with the remaining 50% WONE)

The operation of the contract will be as follows:

* User deposits WONE.&#x20;
* User receives a token share that will mark the proportional amount of LP.&#x20;
* User can harvest their PLTS rewards at any time.&#x20;
* PLTS rewards are stopped around 1 day before adding liquidity to HRMS/WONE.&#x20;
* Investors swap their PLTS to pHRMS.&#x20;
* When liquidity is added the contract performs the following.&#x20;
  * HRMS is purchased with 50% of the bank's internal value.&#x20;
  * Bank with 50% in WONE and 50% in HRMS creates HRMS/WONE LP.&#x20;
  * Once the LP is created it is unlocked for all users who deposited their WONE.&#x20;
  * We will utilize a single block to execute these transactions, avoiding manual errors by the team or external bots that vary the launch price before the bank's WONE purchase is made.&#x20;
* The user, once liquidity is added, can access their LP corresponding to 100% of their deposited value plus the fees generated so far (due to the shared token format). From there they may split their LP (take profit) or deposit it in the farm and generate yield.

### Point of Liquidity Addition

Two percent (2%) of the total HRMS supply will be used to add liquidity. Hermes will provide $275,000 in WONE along with 600,000 HRMS. This will give a launch price of **$0.4583.** As soon as this liquidity is added, the WONE bank's contract will buy with 50% of its deposited value, **raising the floor price of HRMS, returning value to all users proportional to the total amount deposited into the WONE bank**.

{% hint style="info" %}
HRMS Initial Launch Price - $0.4583
{% endhint %}

### What is pHRMS and why are we using it?&#x20;

The two contracts that will be used to make the PLTS - pHERMES swap will be accompanied by a third that will allow users to **exchange their pHRMS for HRMS at a 1:1 ratio**. Shortly after Hermes Defi adds HRMS/ONE liquidity, this swap contract will be opened and users will be able to exchange their pHERMES for HERMES. This allows the project to ensure that they are the first to add liquidity as they will be the only ones to own HRMS and release the token at the right time and price. Hosting private funds in our liquidity launch requires us to be extremely careful with it.&#x20;

{% hint style="info" %}
pHRMS will be exchanged 1:1 with HRMS
{% endhint %}

### How will Hermes Defi handle the transition from PLTS/DAI?

From the time this document is released until the PLTS - pHRMS swap starts, investors are able to remove their PLTS/DAI liquidity from the market.&#x20;

Hermes Defi will continue to incentivize PLTS / DAI LP until the PLTS emissions end, therefore, active investors who farm PLTS/DAI longer will receive more PLTS rewards. However, it is crucial that ALL INVESTORS MUST BREAK PLTS/DAI LPs BEFORE THE SWAP ENDS.&#x20;

{% hint style="danger" %}
ALL INVESTORS MUST BREAK PLTS/DAI LPs BEFORE THE SWAP ENDS.
{% endhint %}

What happens if everyone withdraws their liquidity before the swap ends? The project currently holds over 70% of PLTS / DAI LP so **PLTS swaps will always be guaranteed** (albeit at a higher price impact) throughout this whole process.

### What will happen once the PLTS - pHRMS swap ends?

When the PLTS-pHRMS swap is completed, the project should own all circulating PLTS outside of the project owned LP position. The only existing liquidity will be the one hosted by the project itself. To migrate as much liquidity as possible, **PLTS obtained from the swap will be sold against the project's own liquidity, obtaining 1DAI in exchange**. Once no more 1DAI can be obtained, the LP will be broken and no more PLTS will be traded in the market, **this will bring the token to a price of 0$ and close the PLTS journey on Harmony.**

{% hint style="success" %}
**A journey well spent. Farewell PLTS.**
{% endhint %}

The 1DAI raised will be used in **its entirety** to provide initial HERMES / WONE liquidity, in the case of obtaining private funding and securing the $275,000 through other means, the 1DAI raised will **be sent to the 5/9 multisig**, set up according to Harmony requirements where the funds will be supervised by 5 members of the community.

### Timing

The exact timing of each of these phases and when they will begin will be published at a later date. Currently, the block time of Harmony is quite variable, making it hard to give firm estimates of when these events will all take place. As it is running slow, we will continue to update our docs with our best estimates, and will clearly communicate these steps across all channels. This is a complex and delicate series of actions required to meet all of our objectives. **We apologize for the delay in releasing this document, but hopefully now you understand why it took us so long to do so.**

![](<../.gitbook/assets/PLTS to HRMS (4).png>)
