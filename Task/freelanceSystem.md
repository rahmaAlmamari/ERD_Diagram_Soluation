# **Freelancin gSystem**

## Task requirements:
1. Clients post projects with budgets, deadlines, and required skills. 
2. Freelancers apply to projects and are interviewed. Interviews may include 
   questions, scores, and comments. 
3. Upon selection, the freelancer is assigned a contract with milestones, payment 
   terms, and delivery expectations. 
4. Freelancers submit deliverables tied to milestones, and clients leave reviews after 
   project completion. 
5. Payments may be made per milestone or in full upon project closure. 
6. Both clients and freelancers have profiles with ratings, portfolios, and histories. 

## Task ERD:

![Freelancing System ERD](../image/FreelanceJobMarketplace_TeamWoek.png)

## Task Normaliztion:

![Freelancing System Normaliztion](../image/BankSystemNormaliztion.png)

**1. First Normal Form (1NF) Solution:**
|FreelancerID |FreelancerName |PaymentMode   |
|-------------|---------------|--------------|
|F001         |Yousuf         |Bank Transfer |
|F002         |Mariam         |PayPal        |
|F003         |Khalfan        |Credit Card   |


|FreelancerID |ProjectsID |Projects Name |
|-------------|-----------|--------------|
|F001         |P201       |Website       |
|F001         |P202       |Landing Page  |
|F002         |P203       |Survey        |
|F002         |P204       |Form Upload   |
|F003         |P202       |Landing Page  |
|F003         |P205       |SEO Report    |

|FreelancerID |Skills     |
|-------------|-----------|
|F001         |Web Dev    |
|F001         |UI Design  |
|F002         |Data Entry |
|F003         |Web Dev    |
|F003         |SEO        |
|F003         |Marketing  |

|FreelancerID |ClientName |
|-------------|-----------|
|F001         |SamTech    |
|F002         |QuickData  |
|F003         |SamTech    |
|F003         |WebGo      |



--------------------------------------------------------------------------
**2. Second Normal Form (2NF)  Solution:**
|FreelancerID |FreelancerName |PaymentMode   |
|-------------|---------------|--------------|
|F001         |Yousuf         |Bank Transfer |
|F002         |Mariam         |PayPal        |
|F003         |Khalfan        |Credit Card   |


|ProjectsID |Projects Name |
|-----------|--------------|
|P201       |Website       |
|P202       |Landing Page  |
|P203       |Survey        |
|P204       |Form Upload   |
|P202       |Landing Page  |
|P205       |SEO Report    |

|FreelancerID |ProjectsID |
|-------------|-----------|
|F001         |P201       |
|F001         |P202       |
|F002         |P203       |
|F002         |P204       |
|F003         |P202       |
|F003         |P205       |

|FreelancerID |Skills     |
|-------------|-----------|
|F001         |Web Dev    |
|F001         |UI Design  |
|F002         |Data Entry |
|F003         |Web Dev    |
|F003         |SEO        |
|F003         |Marketing  |

|FreelancerID |ClientName |
|-------------|-----------|
|F001         |SamTech    |
|F002         |QuickData  |
|F003         |SamTech    |
|F003         |WebGo      |