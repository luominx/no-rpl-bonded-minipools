# no-rpl-bonded-minipools

This document explores the introduction of No RPL Bonded Minipools (NRBMs) within the Rocket Pool ecosystem, assessing their potential impact and viability. Our focus is on the integration of NRBMs as a complementary feature to the existing minipool system, without overhauling the current infrastructure. This approach aligns with Lido's strategy of utilizing stETH for Node Operators (NOs) and aims to enhance the Rocket Pool network's efficiency and competitiveness. The proposal includes a detailed analysis of various commission structures, the resultant impact on APR for different stakeholders (rETH holders, effective RPL stakers, and NOs), and the broader implications for the network's stability and growth. The proposed system is designed to attract additional NOs, offer competitive rewards, and maintain a balance between traditional and NRBM staking methods, ensuring a robust and diverse staking environment.


## Idea

- Maintain the existing system, bonding minipools with RPL, to stabilize the network and capitalize on the recent RPIP-30 protocol alignment benefits.
- Prevent burns that reward unstaked RPL, ensuring rewards are limited to active minipool contributors.
- Enhance the rETH Annual Percentage Rate (APR).
- Offer extra incentives to Node Operators (NOs) holding staked RPL, akin to the smoothing pool, boosting minipool creation and reinforcing RPL's value.

The protocol enables NOs to initiate No RPL Bonded Minipools (NRBMs), redirecting a portion of the rETH commission to a pool akin to the smoothing pool. This pool then allocates rewards to actively staked RPL holders.

(Note: The specified commission rates are illustrative and not finalized.)

| Idea     | NO Commission | NRBM NO         | rETH Holders | eff. RPL Stakers | RPL holders | Notes |
| -------- | ------------- | --------------- | ------------ | ---------------- | ----------- | ----- |
| Option 1 | 13%              | 8%              | -13%         | 5%               | -        | Compete with Lido on NRBM commission for NO    |


| Idea     | NO Commission | NRBM NO         | rETH Holders | eff. RPL Stakers | RPL holders | Notes |
| -------- | ------------- | --------------- | ------------ | ---------------- | ----------- | ----- |
| Option 2 | 10%              | 5%              | -9%         | 5%               | -           | Compete with Lido on rETH APR     |


| Idea     | NO Commission | NRBM NO         | rETH Holders | eff. RPL Stakers | RPL holders | Notes |
| -------- | ------------- | --------------- | ------------ | ---------------- | ----------- | ----- |
| Option 3 | 12%              | 7%              | -9%         | 5%               | -           | A mixture from the above     |

#### Additional Protocol Benefits
- NOs utilizing NRBMs gain enhanced rewards compared to solo stakers, benefiting from community support and additional features, potentially including complimentary DVT.
- This model attracts a distinct segment of NOs who, while not engaging with RPL, seek to leverage Rocket Pool's advantages, accepting a marginally lower APR.
- Exposure to the system's robustness, community ethos, and perks may encourage these new NOs to eventually transition to conventional pools.


#### Additional Considerations
- Should Rocket Pool attain 22% of all staked ETH, it could promote traditional RPL-bonded minipools by adjusting rewards: reducing those for NRBMs and enhancing for RPL-backed pools. Additionally, traditional minipools could be prioritized in creation queues.
- The Nodeset model offers a balanced option, presenting a middle ground between NRBM and traditional minipools, with potentially higher rewards than NRBM but more associated risks, and lower rewards but less risk compared to traditional RPL-backed pools (if you fear RPL risk more than smart contract risk). 
- Ultimately, the protocol should aim for simplicity, with enhanced flexibility in commissions, collateral, and bonds for optimal performance. This new minipool variant should not hinder such developments.
- Regarding voting rights, maintaining the status quo, which precludes NRPM-exclusive NOs from participating in governance, may risk community division. Nonetheless, they have the option to operate a standard minipool with bonded RPL to engage in the decision-making process.
- This approach creates a new stakeholder category within Rocket Pool, akin to rETH holders, primarily focused on maximizing their returns with an initial indifference towards RPL's value. Granting voting privileges to this group might be detrimental to RPL's long-term valuation.
