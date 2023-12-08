# Example Calculations

### Assumptions / Variables
- Ratio between ETH staked in NRBMs and Regular Minipools
- All commission percentages

Assumtion:
- Assuming half of Rocket Pool's total staked ETH is in NRBMs, each traditional minipool effectively pairs with an NRBM, receiving 5% of the NO commission. This model presumes uniform collateral levels across all minipools, be it 4, 8, or 16 ETH.

### ETH Staking Rewards for NRBM Operators
The rewards outlined are for a Node Operator (NO) exclusively running NRBMs with a total personal stake of 32 ETH.
##### 8% for NRBM NO
| Idea     | NO Commission | NRBM NO         | rETH holders | eff. RPL Stakers | RPL holders | Notes |
| -------- | ------------- | --------------- | ------------ | ---------------- | ----------- | ----- |
| Option 1 | 13%              | 8%              | -13%         | 5%               | -        |     |

| # minipools | size of pool | NO commission | reward from protocol | reward from rETH holders | total APR |
| ----------- | ------------ | ------------- | -------------------- | ------------------------ | --------- |
| 1           | 32           | 0             | 100%                 | 0                        | 100%      |
| 2           | 16           | 5%            | 50%                  | 8%      (`2*4%`)           | 108%      |
| 4           | 8            | 5%            | 25%                  | 24%      (`4*6%`)          | 124%      |
| 8           | 4            | 5%            | 12.5%                | 56%  (`8*7%`)              | ca. 156%  |
| 16          | 2            | 5%            | 6.25%                | 120%  (`16*7.5%`)           | ca. 220%  |
##### Calculation of column `reward from rETH holders`
The goal is to calculate the total APR by assessing the rewards NOs receive from NRBMs in relation to the overall protocol rewards.

`(100-50)/100*8 = 4`
`(100-25)/100*8 = 6` 
`(100-12.5)/100*8 = 7`
`(100-6.25)/100*8 = 7.5`

##### 5% for NRBM NO
| Idea     | NO Commission | NRBM NO         | rETH holders | eff. RPL Stakers | RPL holders | Notes |
| -------- | ------------- | --------------- | ------------ | ---------------- | ----------- | ----- |
| Option 1 | 10%              | 5%              | -9%         | 5%               | -           |     |

| # minipools | size of pool | NO commission | reward from protocol | reward from rETH holders | total APR |
| ----------- | ------------ | ------------- | -------------------- | ------------------------ | --------- |
| 1           | 32           | 0             | 100%                 | 0                        | 100%      |
| 2           | 16           | 5%            | 50%                  | 5%      (`2*2.5%`)         | 105%      |
| 4           | 8            | 5%            | 25%                  | 15%      (`4*3.75%`)       | 115%      |
| 8           | 4            | 5%            | 12.5%                | 35%  (`8*4.38%`)           | ca. 135%  |
| 16          | 2            | 5%            | 6.25%                | 75%  (`16*4.69%`)          | ca. 175%  |
##### Calculation of column `reward from rETH holders`
`(100-50)/100*5 = 2.5`
`(100-25)/100*5 = 3.75` 
`(100-12.5)/100*5 = 4.38`
`(100-6.25)/100*5 = 4.69`

### ETH Staking Rewards WITHOUT NRBMs
The outlined rewards are for a traditional NO, operating RPL bonded minipools without the NRBM feature added to Rocke Pool, with a total personal stake of 32 ETH.

| # minipools | size of pool | NO commission | reward from protocol | reward from rETH holders | total APR |
| ----------- | ------------ | ------------- | -------------------- | ------------------------ | --------- |
| 1           | 32           | 0             | 100%                 | 0                        | 100%      |
| 2           | 16           | 15%           | 50%                  | 15%      (`2*7.5%`)        | 115%      |
| 4           | 8            | 14%           | 25%                  | 42%      (`4*10.5%`)       | 142%      |
| 8           | 4            | ca. 13%       | 12.5%                | ca. 91%  (`8*11.38%`)      | ca. 191%  |
| 16          | 2            | ca. 12%       | 6.25%                | ca. 180%  (`16*11.25%`)    | ca. 280%  |
##### Calculation for column `reward from rETH holders`
`(100-50)/100*15 = 7.5`
`(100-25)/100*14 = 10.5` 
`(100-12.5)/100*13 = 11.38`
`(100-6.25)/100*12 = 11.38`

### ETH Staking Rewards WITH NRBMs
Presented are the rewards for a traditional NO who operates RPL bonded minipools, in a context where 50% of all staked ETH in the network are allocated in NRBMs.

| # minipools | size of pool | NO commission | NRBMS commission | reward from protocol | reward from rETH holders | reward from NRBMs | total APR |
| ----------- | ------------ | ------------- | ---------------- | -------------------- | ------------------------ | ----------------- | --------- |
| 1           | 32           | 0             | 5%               | 100%                 | 0                        | 0                 | 100%      |
| 2           | 16           | 15%           | 5%               | 50%                  | 15%      (`2*7.5%`)        | 5%   (`2*2.5%`)     | 120%      |
| 4           | 8            | 14%           | 5%               | 25%                  | 42%      (`4*10.5%`)       | 15%  (`4*3.75%`)    | 157%      |
| 8           | 4            | ca. 13%       | 5%               | 12.5%                | ca. 91%  (`8*11.38%`)      | 35%  (`8*4.38%`)    | ca. 226%  |
| 16          | 2            | ca. 12%       | 5%               | 6.25%                | ca. 180% (`16*11.25%`)     | 75%  (`16*4.69%`)   | ca. 355%  |
##### Calculation of column `reward from NRBMs`
`(100-50)/100*5 = 2.5`
`(100-25)/100*5 = 3.75` 
`(100-12.5)/100*5 = 4.38`
`(100-6.25)/100*5 = 4.69`
