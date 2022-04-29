---
description: Set it and forget it, earn UST using single staking of HRMS.
---

# sHRMS

## sHRMS

![](<../.gitbook/assets/sHRMS Cover.png>)

sHRMS or Share Hermes, is a single staking utility for the HRMS token that provides users with yields paid in the UST stablecoin.

### sHRMS Mechanisms

The Hermes Fee Distribution contract receives the platform fee from each swap. With 25% of the received fee, it purchases UST from the available liquidity and sends it to the sHRMS contract. The user earns UST in proportion to their deposited HRMS versus the total HRMS in the sHRMS contract.

![](../.gitbook/assets/sHRMS1.png)

sHRMS is not a Token/Receipt therefore there is no Contract ID for sHRMS. There are no transfer capabilities, users must interact directly with the contract in order to claim UST rewards and deposit or withdraw HRMS. However, sHRMS will be highly accessible as there are no lockup periods and HRMS can be deposit or withdrawn at any time.

### FAQ:

* _How often is UST distributed?_
  * It is constantly refilled.
* _Will there be any fees for staking/depositing?_
  * Yes, sHRMS has a deposit fee mechanism (1% fee) to prevent over-saturation.
* _Where is the fee sent?_
  * The Hermes Protocol Treasury.
* _Is there a time lock for unstaking?_
  * There won't be any timelocks for unstaking or depositing. You can withdraw your HRMS any time through the redeem option.
* _Where do these fees come from?_
  * Trade fees are 0.20% each swap. 0.17% goes to LP providers and 0.03% goes to a contract which swaps 25% of the collected fees to UST and deposits rewards into the sHRMS contract.
* _How much do I earn?_
  * sHRMS Stakers receive rewards proportional to their share of the sHRMS vault. The amount of UST deposited as rewards is directly related to the volume traded on the DEX.

{% hint style="warning" %}
User Reward Rate = userHRMS / totalHRMS \* sHRM Reward Rate.
{% endhint %}

