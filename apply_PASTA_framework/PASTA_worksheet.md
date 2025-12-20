## PASTA worksheet

---

| Stages                                         | Sneaker company                                                                                                                                                                                                                                       |
| :--------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **I. Define business and security objectives** | Make **2-3 notes** of specific business requirements that will be analyzed. _Will the app process transactions? Does it do a lot of back-end processing? Are there industry regulations that need to be considered?_                                  |
| **II. Define the technical scope**             | List of technologies used by the application: _Application programming interface (API) Public key infrastructure (PKI) SHA-256 SQL_ Write **2-3 sentences** (40-60 words) that describe why you choose to prioritize that technology over the others. |
| **III. Decompose application**                 | [Sample data flow diagram](https://docs.google.com/presentation/d/1ol7y79popTFfNHM-90ES-H-i1Lpd0YNvPShxBlXozjg/template/preview?resourcekey=0-DZAkf7Vzh2PXsP-j3oXV-g)                                                                                 |
| **IV. Threat analysis**                        | List **2 types of threats** in the PASTA worksheet that are risks to the information being handled by the application. _What are the internal threats? What are the external threats?_                                                                |
| **V. Vulnerability analysis**                  | List **2 vulnerabilities** in the PASTA worksheet that could be exploited. _Could there be things wrong with the codebase? Could there be weaknesses in the database? Could there be flaws in the network?_                                           |
| **VI. Attack modeling**                        | [Sample attack tree diagram](https://docs.google.com/presentation/d/1FmWLyHgmq9XQoVuMxOym2PHO8IuedCkan4moYnI-EJ0/template/preview?usp=sharing&resourcekey=0-zYPY7AhPJdcClXamlAfOag)                                                                   |
| **VII. Risk analysis and impact**              | List **4 security controls** that you’ve learned about that can reduce risk.                                                                                                                                                                          |

---

1. Business Objectives

- Data privacy
- Secure messaging system
- Quick and easy transaction process

2. Evaluate the apps components
   I think we should focus on the API since that is how users and servers communicate with one another. Because third-party apis are commonly used, it should be an
   area of focus because increase the attack surface of our system.

3. Data flow diagram
   By focusing on the API layer, we can improve security for our customers and users by ensuring input is sanitized and that the user are authenticated and authorized to make a request.

4. Analyze potential threats
   Some pontential threats are XSS attacks and SQL injections performed on the web aplication and unsecured APIs where sensitive data may be leaked.

5. List vulnerabilities that can be exploited by threats
   Payment processing system
   Weak login credentials

6. Attack tree
   A malicious attacker can use SQL injection to gain access to a system if there is a lack of prepared statements and they can also gain access to the system if users
   have weak passwords that are easy to crack.

7. Security controls to reduce risk
   Strong password management
   Encrypt passwords and sensitive data like credit cards
   Implement multi-factor authenication
   Patch, update, or upgrade systems
