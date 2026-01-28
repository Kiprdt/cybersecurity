# Controls and Compliance Assessment 

## Case Study

This is based on a fictional company:

Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide. 

The manager of the IT department has decided that an internal IT audit needs to be conducted. She expresses concerns about not having a solidified plan of action to ensure business continuity and compliance, as the business grows. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).   

The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment. The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.

Your task is to review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist. 

## Scenario
Botium Toys: Scope, Goals, and Risk Assessment Report

### Scope 

The scope of this audit is defined as the entire security program at Botium Toys. This includes their assets like employee equipment and devices, their internal network, and their systems. You will need to review the assets Botium Toys has and the controls and compliance practices they have in place.

### Goals
Assess existing assets and complete the controls and compliance checklist to determine which controls and compliance best practices need to be implemented to  improve Botium Toys’ security posture.

### Current assets
Assets managed by the IT Department include: 
* On-premises equipment for in-office business needs  
* Employee equipment: end-user devices (desktops/laptops, smartphones), remote workstations, headsets, cables, keyboards, mice, docking stations, surveillance cameras, etc.
* Storefront products available for retail sale on site and online; stored in the company’s adjoining warehouse
* Management of systems, software, and services: accounting, telecommunication, database, security, ecommerce, and inventory management
* Internet access
* Internal network
* Data retention and storage
* Legacy system maintenance: end-of-life systems that require human monitoring 

### Risk assessment

#### Risk description
Currently, there is inadequate management of assets. Additionally, Botium Toys does not have all of the proper controls in place and may not be fully compliant with U.S. and international regulations and standards. 

#### Control best practices
The first of the five functions of the NIST CSF is Identify. Botium Toys will need to dedicate resources to identify assets so they can appropriately manage them. Additionally, they will need to classify existing assets and determine the impact of the loss of existing assets, including systems, on business continuity.

#### Risk score
On a scale of 1 to 10, the risk score is 8, which is fairly high. This is due to a lack of controls and adherence to compliance best practices.

#### Additional comments
The potential impact from the loss of an asset is rated as medium, because the IT department does not know which assets would be at risk. The risk to assets or fines from governing bodies is high because Botium Toys does not have all of the necessary controls in place and is not fully adhering to best practices related to compliance regulations that keep critical data private/secure. Review the following bullet points for specific details:
* Currently, all Botium Toys employees have access to internally stored data and may be able to access cardholder data and customers’ PII/SPII.
* Encryption is not currently used to ensure confidentiality of customers’ credit card information that is accepted, processed, transmitted, and stored locally in the company’s internal database. 
* Access controls pertaining to least privilege and separation of duties have not been implemented.
* The IT department has ensured availability and integrated controls to ensure data integrity.
* The IT department has a firewall that blocks traffic based on an appropriately defined set of security rules.
* Antivirus software is installed and monitored regularly by the IT department. 
* The IT department has not installed an intrusion detection system (IDS).
* There are no disaster recovery plans currently in place, and the company does not have backups of critical data. 
* The IT department has established a plan to notify E.U. customers within 72 hours if there is a security breach. Additionally, privacy policies, procedures, and processes have been developed and are enforced among IT department members/other employees, to properly document and maintain data.
* Although a password policy exists, its requirements are nominal and not in line with current minimum password complexity requirements (e.g., at least eight characters, a combination of letters and at least one number; special characters). 
* There is no centralized password management system that enforces the password policy’s minimum requirements, which sometimes affects productivity when employees/vendors submit a ticket to the IT department to recover or reset a password.
* While legacy systems are monitored and maintained, there is no regular schedule in place for these tasks and intervention methods are unclear.
* The store’s physical location, which includes Botium Toys’ main offices, store front, and warehouse of products, has sufficient locks, up-to-date closed-circuit television (CCTV) surveillance, as well as functioning fire detection and prevention systems.
#### Additional Info 

In Cybersecurity, control types can be classified in three ways: 
1. Administrative/Managerial controls
2. Technical controls
3. Physical/Operational controls

Control types (providing defense and protecting assets) include, but are not limited to:
1. Preventative (preventing an incident from occurring in the first place)
2. Corrective (restoring an asset after an incident)
3. Detective (Determining whether an incident has occurred or is in progress)
4. Deterrent (Discouraging attacks)

## Controls Assessment Checklist

Does Botium Toys currenly have this control in place? 

| Yes / No | Control | Explanation |
| :-------        |    :---:   | :---     |
| No | Least Privilige | All employees have access to customer data. Privileges should be limited to responsibilities to reduce the risk of leakage |
| No | Disaster Recovery Plan | The lack of a disaster recovery plan can lead to disruption of business continuity.  |
| No | Password policies  | Employee password requirements are minimal that could allow a threat actor to more easily access secure data |
| No | Separation of duties | Access controls for separation of duties have not been implemented. The lack of this control allows a single individual to perform critical actions that could cause significant damage to the organization |
| Yes | Firewall | The existing firewall blocks traffic based on an appropriately defined set of security rules |
| No | Intrusion detection system (IDS) | An IDS can help identify possible intrusions by threat actors |
| No | Backups | It's need to have backups of critical data to ensure business continuity in the case of a breach. |
| Yes | Antivirus Software | Antivirus software is installed and monitored regularly by the IT department | 
| No | Manual monitoring, maintenance, and intervention for legacy systems | There is no regular schedule for monitoring legacy systems, and policies related to intervention are unclear. |
| No | Encryption | Encryption is not currently used but implementing it would provide greater confidentiality of sensitive information. |
| No | Password management system | There is no password management system currently in place but implementing this control would improve security and employee productivity by reducing password fatigue. |
| Yes | Locks (offices, storefront, warehouse) | The store’s physical location, which includes Botium Toys’ main offices, store front, and warehouse of products, has sufficient locks. |
| Yes | Closed-circuit television (CCTV) surveillance | There is up-to-date closed-circuit television (CCTV) surveillance |
| Yes | Fire detection/prevention (fire alarm, sprinkler system, etc.) | There is functioning fire detection and prevention systems. |

## Compliance Checklist
Does Botium Toys currenly adhrere to this compliance best practice? 

* Payment Card Industry Data Security Standard (PCI DSS)

| Yes/ No | Best Practice | Explanation |
| :---        |    :---:   | :---     |
| No | Only authorized users have access to customers’ credit card information.  | Currently, all employees have access to internally stored data, which may include cardholder information. |
| No | Credit card information is stored, accepted, processed, and transmitted internally, in a secure environment. | Information is stored locally in an internal database without encryption |
| No | Implement data encryption procedures to better secure credit card transaction touchpoints and data.  | Encryption is not currently used for credit card information that is accepted, processed, transmitted, or stored. | 
| No | Adopt secure password management policies. | Current password requirements are nominal and there is no centralized management system |

* GDPR
  
| Yes/ No | Best Practice | Explanation |
| :---        |    :---:   | :---     |
| No | E.U. customers’ data is kept private/secured. | Confidentiality is at risk because encryption is not used and access controls like least privilege are missing. |
| Yes | There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach. | The IT department has established a breach notification plan specifically for E.U. customers |
| No | Ensure data is properly classified and inventoried. | While assets are listed, they have not yet been classified to determine their impact on business continuity. |
| Yes | Enforce privacy policies, procedures, and processes to properly document and maintain data. | Privacy policies and processes have been developed and are enforced among department members. |

* System and Organizations Controls 

| Yes/ No | Best Practice | Explanation |
| :---        |    :---:   | :---     |
| No | User access policies are established | Access controls for least privilege and separation of duties have not been implemented |
| No | Sensitive data (PII/SPII) is confidential/private. | Encryption is not used locally, and all employees currently have access to sensitive internal data |
| Yes | Data integrity is consistent, complete, accurate | The IT department has integrated controls to ensure data integrity | 
| No | Data is available to individuals authorized to access it. | Data is available to all employees rather than being restricted to only authorized individuals. |

## Recommendations (optional):
Audit results indicate that current security policies and controls do not guarantee the absence of fines, business continuity, or a low probability of sensitive data compromise. Without implementing the recommended controls, the company faces significant financial risks and potential loss of customer trust.

* Password policies must be refined to incorporate minimum security requirements, such as complexity and length standards.

* Password management should be centralized, requiring the use of a password manager to reduce password fatigue and improve overall security.

* It is essential to define a Disaster Recovery Plan (DRP) and implement system backups to ensure the company can recover from a breach or system failure.

* The principle of Separation of Duties must be enforced to ensure that access to PII and SPII is restricted to authorized personnel only.

* The Principle of Least Privilege must be implemented to prevent users from holding unnecessary administrative functions and to reduce the impact of malicious insiders or compromised accounts.

* Encryption is mandatory for all locations storing sensitive information, including customer credit card data and PII.

* Intrusion Detection Systems (IDS) should be deployed to identify and mitigate potential threats in real-time.

* A clear schedule and defined methods for monitoring and maintaining legacy systems must be established to address identified vulnerabilities.

* Botium Toys needs to properly classify assets to identify additional controls required to improve their security posture and better protect sensitive information.
