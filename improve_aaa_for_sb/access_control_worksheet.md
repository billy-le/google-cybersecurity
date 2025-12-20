## Access controls worksheet

---

|                                   | Note(s)                                                                                                                                               | Issue(s)                                                                                                                                     | Recommendation(s)                                                                                                                                          |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Authorization /authentication** | **Objective:** List 1-2 pieces of information that can help identify the threat: _Who caused this incident? When did it occur? What device was used?_ | **Objective:** Based on your notes, list 1-2 authorization issues: _What level of access did the user have? Should their account be active?_ | **Objective:** Make at least 1 recommendation that could prevent this kind of incident: _Which technical, operational, or managerial controls could help?_ |

### Notes

Who caused this incident?
The contractor, Robert Taylor Jr., has a compromised system with the same IP address as the event.

When did it occur?
The incident occured on Oct 3rd, 2023 at 8:29 AM.

What device was used?
The device named Up2-NoGud was used in the attack.

### Issues

What level of access did the user have?
The user's account has an access level of admin.

Should their account be active?
Their account should not be active since their end date was December 27, 2019 and the attack happened in the year 2023.

### Recommendations

Which technical, operational, or managerial controls could help?

There are several recommendations we can implement to improve the security of this business. We can implement the Principle of Least Privelege and also Separation of Duties.
The contractor should not have admin access and should not have the ability to make deposits from the company's account. To further improve on PoLP and Separation of duties
we can use a role-base authorization controls to limit which users has access to resources and what actions they can perform based on their roles. Since this was
a contractor with a role of legal/attorney that was compromised, we create a system where any new contractor with the same role is only given access to what they need to perform their duties.
