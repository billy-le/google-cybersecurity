## Risk register

---

### **Operational environment:**

The bank is located in a coastal area with low crime rates. Many people and systems handle the bank's data—100 on-premise employees and 20 remote employees. The customer base of the bank includes 2,000 individual accounts and 200 commercial accounts. The bank's services are marketed by a professional sports team and ten local businesses in the community. There are strict financial regulations that require the bank to secure their data and funds, like having enough cash available each day to meet Federal Reserve requirements.

| Asset | Risk(s)                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Likelihood | Severity      | Priority |
| :---- | :----------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ------------- | -------- |
| Funds | Business email compromise                                                                              | _An employee is tricked into sharing confidential information._                                                                                                                                                                                                                                                                                                                                                                                                       | Certain    | Castastrophic | 9        |
|       | Compromised user database                                                                              | _Customer data is poorly encrypted._                                                                                                                                                                                                                                                                                                                                                                                                                                  | Likely     | Moderate      | 4        |
|       | Financial records leak                                                                                 | _A database server of backed up data is publicly accessible._                                                                                                                                                                                                                                                                                                                                                                                                         | Rare       | Moderate      | 2        |
|       | Theft                                                                                                  | _The bank's safe is left unlocked._                                                                                                                                                                                                                                                                                                                                                                                                                                   | Rare       | Low           | 1        |
|       | Supply chain disruption                                                                                | _Delivery delays due to natural disasters._                                                                                                                                                                                                                                                                                                                                                                                                                           | Rare       | Moderate      | 2        |
| Notes | _How are security events possible considering the risks the asset faces in its operating environment?_ | Considering the coastal location and low crime rate area, security events are still possible through exploitation of weak security surrounding employees. If employees are not well-trained, there could be possible security breaches like unlocked safes and registers, opening phishing emails and compromising their machines, and more. A natural disaster can unfold too since the location is close by the ocean where possible floods or tsunamis can happen. |            |               |          |

**Asset:** The asset at risk of being harmed, damaged, or stolen.  
**Risk(s):** A potential risk to the organization's information systems and data.  
**Description:** A vulnerability that might lead to a security incident.  
**Likelihood:** Score from 1-3 of the chances of a vulnerability being exploited. A 1 means there's a low likelihood, a 2 means there's a moderate likelihood, and a 3 means there's a high likelihood.  
**Severity:** Score from 1-3 of the potential damage the threat would cause to the business. A 1 means a low severity impact, a 2 is a moderate severity impact, and a 3 is a high severity impact.  
**Priority:** How quickly a risk should be addressed to avoid the potential incident. Use the following formula to calculate the overall score: **Likelihood x Impact Severity \= Risk**

## Sample risk matrix

---

|           | Low 1 | Moderate 2 | Catastrophic 3 |
| :-------: | :---: | :--------: | :------------: |
| Certain 3 |   3   |     6      |       9        |
| Likely 2  |   2   |     4      |       6        |
|  Rare 1   |   1   |     2      |       3        |
