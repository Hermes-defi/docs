---
description: Interested in applying for a Hermes Dual Farm? Read on.
---

# Dual Farms

## What is a Hermes Dual Farm?&#x20;

Dual Farms are an innovative farming mechanism that allows farmers to receive **TWO** reward tokens (HRMS and one supplied by the partner) at independent rates. Our dual farm contracts were inspired by TraderJoe, the leading DEX on AVAX. This allows for **greater complexity**, **higher APR**, **less direct sell pressure**, and **launchpad-like abilities** compared to traditional farms that can only reward a single token.

{% hint style="info" %}
Note: This document is extremely thorough, please ensure you take the proper amount of time required to fully review all aspects of our Dual Farm system before applying.
{% endhint %}

You can view our [code surrounding our dual farms ](https://github.com/Hermes-defi/hermes-swap/blob/main/contracts/MasterChefHermesV2.sol)(currently under review by [Certik](https://www.certik.com/projects/hermes-defi), who has reviewed projects with a combined TVL of 288B).

### Part 1: The Application Process

_How can my project apply for a Dual Farm on Hermes?_&#x20;

1. **Application and Discussion.** After reading this documentation in its entirety, the Partner will fill out [a partnership application](https://forms.gle/7uu9zgcCfjE3Vxoa6) that details their project and desired farm type. Hermes will follow up within 3 days with an initial project assessment (IPA) and schedule a meeting with project leaders. If an agreement is reached, the listing will be scheduled.
2. **Fund Transfer and Farm Creation.** The evaluation of The Partner tokens and HRMS will be made shortly before the beginning of the farming period. The Partner will send Hermes the agreed upon quantity of Partner Tokens. The farming contract will be filled with HRMS and the Partner Token at the agreed upon ratio. The farming reward period will be set (both start and end).
3. **Farming Period.** At the agreed upon date, the farm will go live and begin to earn rewards. Hermes and the Partner will both advertise this to their community. Once farming begins, users earn both HRMS and the Partner Token based on their share of the total amount staked in the Dual Farm. Rewards are emitted every block and can be claimed at any time. **HRMS earned from dual farms will be fully unlocked**. Custom solutions surrounding rewarding locked partner tokens can be discussed. Type A Dual Farms reward 75% Partner Token and 25% HRMS while Type B Dual Farms reward 50% Partner Token and 50% HRMS.
4. **Farm Effectiveness Reporting.** After the conclusion of the Dual Farm (15 or 30 days), Hermes will provide an analytics report detailing the success metrics of the Dual Farm. This report will contain things such as: Number of unique wallets participating, LP TVL over time, Trading Volume Report, and more.

### Part 2: Hermes Dual Farm Tokenomics

Partners can choose to host their liquidity in three different LP pairs:&#x20;

* Partner Token / WONE&#x20;
* Partner Token / UST (recommended over USDC)
* Partner Token / USDC

#### Emissions and allocation to Dual Farms:

Hermes has allocated 6% of our [total supply](../tokenomics/hermes-token-distribution.md) to help bolster our DEX liquidity through partnerships and dual farms. Over the next 2.5 years (30 months), 1,800,000 HRMS tokens will be released through dual farms. Therefore, we will be able to **distribute 60,000 tokens each month** or 30,000 tokens every 15 days.&#x20;

#### Identifying the Duration and Allocation breakdown of your Dual Farm:

{% hint style="info" %}
At this time, we offer **two durations** and **two allocations**. Partners will be able to choose their preferred Dual Farm type from the following four options:
{% endhint %}

* Dual Farm Type A1 - 75/25 (PartnerToken/HRMS) for 15 Days
* Dual Farm Type A2 - 75/25 (PartnerToken/HRMS) for 30 Days
* Dual Farm Type B1 - 50/50 (PartnerToken/HRMS) for 15 Days
* Dual Farm Type B2 - 50/50 (PartnerToken/HRMS) for 30 Days

In addition to the difference in duration (15/30 days) and ratio of partner to Hermes tokens, there is a slight difference in the **fee structure** between Type A and B Dual Farms to help offset the increased HRMS sell pressure. In order to maintain the stability and pace of HRMS dual farm emissions, we will make fixed allocations of the number of HRMS tokens, not their dollar value. This also means that we will only be able to accommodate a limited number of dual farms every month. Please plan ahead and get in touch with us early to help secure your spot.

#### Dual Farm Examples:

Example A: There is an already scheduled Farm for 1 month (30,000 HRMS tokens) Only 30,000 HRMS remains for dual farm emissions. This may be split between one other 1-month long dual farm (30,000 HRMS) or two 15-day dual farms (15,000x2 HRMS).

Example B: There is an already scheduled Farm for 15 days (15,000 HRMS tokens) Only 45,000 HRMS remains for dual farm emissions. This may be split between one 1-month long dual farm with an additional 15-day dual farm (30,000 + 15,000) or into three 15-day dual farms (15,000x3 HRMS)

Determining criteria during negotiations: Our weighting system will be based upon three factors to prioritize farms:&#x20;

1. Those who wish to pursue the 75% / 25% allocation farm
2. Those who elect choose a 30 day dual farm
3. All following potential partners

{% hint style="info" %}
You can play with the [Dual Farm Calculator](https://docs.google.com/spreadsheets/d/1EiA28hDV6dayI9WqesiEubqEIDX-6jz-sV4jMF4oYUg/edit?usp=sharing) to get a better idea of APR, reward amounts, fees, etc.
{% endhint %}

### Part 3: Fees

#### Breaking down the fees for Hermes’ Platform:&#x20;

At the time of token transfer from the partner, Hermes will calculate the number of partner tokens required based on the current value of the HRMS token allocation for the dual farm duration. This partner token will EXCLUSIVELY be placed into the dual farm. Additional fees will be paid to Hermes depending on the type of farm Type A (75:25) or Type B (50:50).

**Dual Farm Type A (75:25)** Additional fee equivalent to 23% of farm allocation.&#x20;

66.6% to Hermes Developers, 16.6% to Hermes Treasury, 16.6% to stake xHRMS Rewards

**Dual Farm Type B (50:50)** Additional fee equivalent to 31% of farm allocation.

55.5% to Hermes Developers, 22.2% to Hermes Treasury, 22.2% to stake xHRMS Rewards

### Part 4: Limitations

_What restrictions are there for dual farm applications?_

**Subject to code review.**&#x20;

As part of our commitment to our userbase for safety, transparency, and efficiency, we may request to review your source code, even if it is not open source. We do this to help protect Hermes' image and trustworthiness as a DEX and launch platform. We wish to uphold 100% transparency for our users and ask that you respect this as well. If your protocol has been audited and there is a report available, this may be accepted in lieu of our own investigation.&#x20;

**Malicious tokens will not be accepted.**

Concerns of Rug-pulls or maliciously designed tokens is a concern for our dual farms as well. With this knowledge, we will look for aspects in how the token will maintain utility to ensure that it has a forward-thinking aspect behind its creation. **We will not host tokens that are unable to offer some aspect to this.**

**Macroeconomic token outlook**

In addition to not supporting tokens that are inherently malicious, we will work with the potential partner to better understand the macroeconomic outlook of their tokens liquidity. As Hermes is making an investment into the partner project (both in terms of our treasury and emissions from the HRMS token), **we want to work with partners to have their project succeed**. You'll get access to some of the brightest DeFi minds on Harmony to help guide you to how hosting your liquidity on Hermes can be mutually beneficial.



## Questions? Let's talk!

Reach out to Valleyrider, Austin, Aaron, or Maba on [Discord](https://discord.gg/hermesdefi), or to the official Hermes [Twitter](https://twitter.com/hermesdefi), [Reddit](https://www.reddit.com/user/HermesDeFi), or [email](mailto:austin@hermesdefi.io).

