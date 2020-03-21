# Scope Definition

### Introduction
#### Document Purpose
This Document has a number of key purposes:
- To explain the need for this project to be progressed – the problem or opportunity.
- To understand any specific drivers or constraints that apply to the project and to justify assumptions on why IT and manual solutions are needed.
- To record the project objectives and high level requirements (functional and non-functional).
- To establish and baseline the scope of the project, including in-scope processes and classes of data.
This document will NOT describe a solution.  In particular, requirements should not mention specific IT applications, components or interfaces between them.  Those things however could be mentioned in accompanying information such as background information etc where appropriate.

#### Target Audience
All business and IT stakeholders.

### Business Context
#### Project Background
Currently the existing website does not offer customers the opportunity to manage their accounts online.  Customers therefore contact Customer Services for all aspects of account management.  

A secure website portal (My Account) is required to enable customers to self-service and manage their accounts online without the need to contact the Customer Services Team.  This will result in a reduction in the number of Customer Services calls received.

Following the launch of the new BAYV website in Dec 2016, further improvements are required to enhance the functionality of the website in line with our competitor sites.


#### Problem/Opportunity Statement
This project will enhance the customer experience by giving them access to account information, payment options and customer request functionality that previously hasn’t been available.  Customers will be able to access the information 24/7, whereas, currently they can only contact Customer Services within business hours.

The volume of non-value add calls within Customer Services are too high, (approx. 35% of calls relate to customers reporting service issues and requesting balance enquiries or statement queries).  With the introduction of online account management ‘My Account’ the customer would be able to self-serve rather than calling the Customer Services Team.


### Business Objectives
|Ref | Title	Description|
|---|---|
|BOJ01 |	Improved website functionality	Increase website functionality to allow customers to self-serve 24/7 via a My Account secure facility.|
|BOJ02 |	Process optimisation – Customer Services.  Remove non-value add steps from the Customer Services Team by reducing the call volume.|
|BOJ03 |	Customer online account management	Allow customers to manage their BAYV account online with the facility to check balance information make payments, raise service and meter calls.| 
|BOJ04 |	Sales Process - My Account set up	Optional ‘my account’ set up as part of the online sales process.|


### Critical Success Factors
|Ref |	Title |	Description|
|---|---|---|
|CSF01 | Website functionality | The website must secure and maintain detailed logs of all customer activity.|
|CSF02 | Data accuracy | Live customer data must be accurate.|
|CSF03 | Account log in and password resets | Customer login infrastructure must be sufficient so that there is no commercial burden on maintaining customer login, password resets etc.|
|CSF04 | Process optimisation |	My Account will enable process optimisation of existing customer service processes.|
|CSF05 | Customer engagement |	My account must offer customers an easy to use portal that is beneficial in managing their accounts.|
|CSF06 | Sales completion rates | No material reduction in sales completion rates.|

### Key Assumptions
- Customers will be required to set up ‘My Account’ as part of the online sales process.
- Customers will be required to set up a Direct Debit [DD] as part of the online sales process. 
- My account ‘customer requests’ will feed into the appropriate system for internal action.
- Live customer data will be accurate.
- BAYV Website and internal system changes can be made within the project timescale.
- Changes to internal processes can be designed/communicated/trained within the business.
- Resource is available for all aspects of the project.
- Funding is available for the project.

### Drivers and Constraints
Scope -  The project needs enhance to website functionality enabling customers to self-serve.
Quality – All requirements must be well defined to facilitate the build quality of the design.
Time – The project must go live on (date TBD)
Cost -  Funding is available for all elements of the project


|Driver | Descriptions of importance or any constraints that are relevant | Priority
|---|---|---|
|Time |	Earliest possible delivery |3 |
|Cost |	Within funding budget | 4 |
|Quality | Customer information must be of a quality that adds value to the customer’s experience |2| 
|Scope | Reduction in Customer Services calls required asap | 1 |

### Definition of Scope
#### Processes
|Processes|Description of Impact|
|---|---|
|Sales | Customers will be given the option to set up ‘My Account’ as part of the online sales process.|
|Payments | Online payments will be available to customer who have set up my account.|
|Direct Debits | Customers will be required to set up a DD as part of the sales process.|
|Direct Debits | Customers will have the option to set up a DD if they are currently not a DD customer.|
|Service Requests| Customers will be able to self-serve when reporting product faults (reduction in Customer Services calls).|
|Meter Calls | Customers will be able to self-serve when requesting a meter call (reduction in Customer Services calls).|
|Balance/ payment enquiries | Customers will be able to self-serve when requesting Balance or payment enquiries (reduction in Customer Services calls).|
|Arrears | Customers will be notified of arrears and will be able to make payments (improvement in Arrears and reduction in Customer Services/Telecollections calls).|

Process Map of the impacted process can be found below:

#### Customer Segment
|Customer Segment| Description of Impact|
|---|---|
|All|My Account will be available to all customers.|

#### Out of Scope
Further enhancements scoped for phase 2 and 3 ie Downloading documents, viewing account history, additional self-service function etc

### High Level Requirements
#### High Level Functional Requirements
|Ref| Title| Description| Priority (MSC)|Related Req(s)|
|---|---|---|---|
|FR01|	Website – Customer Log In|	Secure customer account login’s providing sufficient security of financial and personal information held on the customer (data protection).|	M|	UC-13|
|FR02|	Website – My Account Summary|	New screens to display a summary of the customers’ accounts including next payment amount, outstanding balance and any arrears.|	M|	UC-01|
|FR03|	Website – My Meter|	New screens to display the customers Meter information and request a Meter visit.|	M|	UC-05|
|FR04|	Website – My Payments|	New screens to display the customers Payment information and options to make a payment or set up a DD.|	M|	UC-04|
|FR05|	Website – My Products|	New screens to enable customers to a view their agreements and product level information with the option of reporting a fault on a product covered by AS/EPS payments.|	M|	UC-18|
|FR06|	Website – My Details|	New screens to enable customers to view the personal information held with the option to change marketing preferences.|	M|	UC-16|
|FR07|	Website – My Orders|	New screens to allow customer to view the status of their orders.|	M|	UC-15|
|FR08|	Website – Card Payments|	New screens to allow the customer to make an online card payment.|	M|	UC-14 (FR12)|
|FR09|	Website – Direct Debits|	New screens to allow the customer to set up DD.|	M|	UC-17 (FR12)|
|FR10|	Website – Service Calls|	New screens to allow customers to report a faulty product (service call) and track the progress of a fault|	S| |
|FR11|	Website - Arrears|	New screens to display the amount of arrears on an account and present an option to bring the account up to date|	M|	UC-19|
|FR12|	Website - Styling|	Third party supplier pages to be styled as BAYV.|	S|	FR04, FR08|
|FR13|	Oracle	Information held in Oracle will be made available to the customer on the website.|	M|	FR02 – FR11|

### High Level Data Requirements
Ref	Title	Description	Priority
(MSCW)	Related Requirements
DR01	Customer Logins	Security data fields required for customer verification with Oracle.	M	FR01
DR02	Website/ Oracle	Customer Data to be displayed on the website.	M	FR02 - FR011, FR13
DR03	Bottomline	DD set up data fields to be available on the website.	M	FR09, FR10
DR04	Elevon	Data fields for customer card payments must be available on the website.	M	FR08, FR10

### High Level Non-Functional Requirements
Ref	Title	Description	Priority
(MSCW)	NFR Type	Related Req’s
NFR01	Website	Additional links to third parties styled as BAYV website	M	Look and feel	FR10
NFR02	Website	Simple customer instructions on website pages	M	Usability 	FR01 – FR09
NFR03	Website	Timely response	S	Performance – Speed	FR11
NFR04	Website	24/7 availability same as the website	S	Availability - Hrs	FR11
NFR06	Customer	Enhanced customer impact	S	Customer Impact	
NFR07	Staff	Minimal staff impact	S	Staff Impact	
NFR08	L & R	Compliant to all L & R requirements	M	Legal and Regulatory	FR01

### Potential Extent of IT solution

### Naming Conventions
|Term| Description|
|---|---|
|DD| Direct Debit|
|L & R| Legal and Regulatory|
	




