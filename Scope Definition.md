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
There is no main-stream online resource available to present medical research to a non-academic audience.  Users are therefore reliant on the plethora of opinion and hear-say when seeking answers to their health and medical questions.  

A deliverable is required to produce summarised and paraphrased briefs on a number of key health topics.  It is envisaged that the briefs will be presented via a short video or infograhpic through social media.  The process will need to be automated where possible with limited manual intervention or review.  This will result in an increased number of articles, enhanced accuracy, and it is hoped, and greater view-count.

Following the launch of the HillsHealth.org website in 2012, this project will automate what was previously a manual solution, and deliver the summaries in a contemporary and salient manner.

#### Problem/Opportunity Statement
This project will enhance the on-line experience by giving users access to evidence-based health and medical information that is both summarised and paraphrased.  The solution will engage the user via social-media, and provide the briefs via short on-line videos or infographics.  Output is expected to be automated with limited manual review.  This will allow for a greater volume of articles that is currently possible via the current HillsHealth.org site.

The volume of fake and mis-leading online articles covering health and medical opinion makes it difficult for the user to differentiate fact from fiction.  Trials published in medical journals are the gold-standard of health and medical information and should be accesible to all.  However, the academic slant of these papers make them incomprehensible to the non-scholar, and with a firewall preventing full access to all but a few sites, a solution is required to bring the informaion to the layman and provide an on-line audience with a better alternative to the current volume of mis-leading, and often dangerous, medical and health information. 


### Business Objectives
|Ref | Title|	Description|
|---|---|---|
|BOJ01 |	Process Optimisation |	Automate the summarisaton and paraphrasing of medical papers from scientific journals|
|BOJ02 |	Content Production | Present summaries in a contemporary, clear, and eye-catching manner|
|BOJ03 |	Content Delivery| Use social media to deliver summaries to the wider audience| 
|BOJ04 |	Content Optimisation| Use keywords and other SEO techniques to promote the summaries|


### Critical Success Factors
|Ref |	Title |	Description|
|---|---|---|
|CSF01 | Automation | The deliverable must be able to summarise and paraphrase medical papers.|
|CSF02 | Data accuracy | Summaries must accurately reflect the source paper.|
|CSF03 | Content Delivery | The output must be presented via motion graphic or infographic|
|CSF04 | User engagement | The deliverable must be clear and offer customers an easy to understand solution.|
|CSF06 | View rates | Increase in views (metric TBC)|

### Key Assumptions
- Customers will be required to set up ‘My Account’ as part of the online sales process.
- Customers will be required to set up a Direct Debit as part of the online sales process. 
- My account ‘customer requests’ will feed into the appropriate system for internal action.
- Live customer data will be accurate.
- x Website and internal system changes can be made within the project timescale.
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
|---|---|---|---|---|
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
|FR12|	Website - Styling|	Third party supplier pages to be styled as x.|	S|	FR04, FR08|
|FR13|	Oracle|	Information held in Oracle will be made available to the customer on the website.|	M|	FR02 – FR11|

### High Level Data Requirements
|Ref|	Title|	Description|	Priority (MSCW)|	Related Requirements|
|---|---|---|---|---|
|DR01|	Customer Logins|	Security data fields required for customer verification with Oracle.|	M|	FR01|
|DR02|	Website/ Oracle|	Customer Data to be displayed on the website.|	M|	FR02 - FR011, FR13|
|DR03|	Bottomline|	DD set up data fields to be available on the website.|	M|	FR09, FR10|
|DR04|	Elevon|	Data fields for customer card payments must be available on the website.|	M|	FR08, FR10|

### High Level Non-Functional Requirements
|Ref|	Title|	Description|	Priority (MSCW)|	NFR Type|	Related Req’s|
|---|---|---|---|---|---|
|NFR01|	Website|	Additional links to third parties styled as BAYV website|	M|	Look and feel|	FR10|
|NFR02|	Website|	Simple customer instructions on website pages|	M|	Usability |	FR01 – FR09|
|NFR03|	Website|	Timely response|	S|	Performance – Speed|	FR11|
|NFR04|	Website|	24/7 availability same as the website|	S|	Availability - Hrs|	FR11|
|NFR06|	Customer|	Enhanced customer impact|	S|	Customer Impact	|
|NFR07|	Staff|	Minimal staff impact|	S|	Staff Impact|	
|NFR08|	L & R|	Compliant to all L & R requirements|	M|	Legal and Regulatory|	FR01|

### Potential Extent of IT solution

### Naming Conventions
|Term| Description|
|---|---|
|DD| Direct Debit|
|L & R| Legal and Regulatory|
	




