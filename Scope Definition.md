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
|CSF06 | Increase in user metrics | Increase in views (metric TBC)|

### Key Assumptions
- Access to medical journals is available (either full access or abstract).
- No project timescale applies.
- Resource is available for all aspects of the project.
- Funding is available for the project.

### Drivers and Constraints
Scope -  The project needs to automate the summarisation and paraphasing of medical papers, and present online via a graphic.
Quality – All requirements must be well defined to facilitate the build quality of the design.
Time – The project must go live on (date TBD)
Cost -  Funding is available for all elements of the project


|Driver | Descriptions of importance or any constraints that are relevant | Priority
|---|---|---|
|Time |	Earliest possible delivery |4 |
|Cost |	Within funding budget | 3 |
|Quality | Summaries must be of a quality that adds value to the customer’s experience |2| 
|Scope | Provide summaries of medical papers and publish online | 1 |

### Definition of Scope
#### Processes
|Processes|Description of Impact|
|---|---|
|Data Mining | Extract medical papers from scientific journals specific to a chosen topic.|
|Data Wrangling | Transform the medical papers to a summarised and paraphrased brief. Briefs will be converted to a handful of points covering participants, study and results.|
|Data Presentation.| Briefs will be presented via a graphic (either motion or infographic)|
|Manual Sanity Check| The editor will review the outcome for accuracy and suitable presentation|
|Summary Posted | The sumarised and paraphrased graphic will be posted to a suitable social media site (TBC).|

Process Map of the impacted process can be found below:

#### Customer Segment
|Customer Segment| Description of Impact|
|---|---|
|All|The briefs will be universally available via social media and will cover a handful of key health topics..|

#### Out of Scope
Further analysis of the data collected, i.e. systematic reviews of collected summaries

### High Level Requirements
#### High Level Functional Requirements
|Ref| Title| Description| Priority (MSC)|Related Req(s)|
|---|---|---|---|---|
|FR01|	Data Mining| Data Mine relevant articles from a selection of medical journals.  The chosen journals will be based on the impact factor, with studies chosen based on the Jadad criteria.|	M|	UC-01|
|FR02|	Article analysis and refinement|	A soluion that will summarise and paraphrase the articles as provided in FR01.|	M|	UC-|
|FR03|	Create Summary Visualisation|	A solution that will enable to summary created in FR02 to be visualised|	M|	UC-|
|FR04|	Post summaries on-line|	The summaries will be posted to social media and other on-line outlets that are relevant to the chosen topic.|	M|	UC-|

### High Level Data Requirements
|Ref|	Title|	Description|	Priority (MSCW)|	Related Requirements|
|---|---|---|---|---|
|DR01|	Customer Logins|	Summaries must reflect the information provided in the journal paper.|	M|	FR00|


### High Level Non-Functional Requirements
|Ref|	Title|	Description|	Priority (MSCW)|	NFR Type|	Related Req’s|
|---|---|---|---|---|---|
|NFR01|	Algorithm|	Timely response to request for summaries|	S|	Performance – Speed|	FR01|
|NFR02|	Summaries|	24/7 availability (both input and output)|	S|	Availability - Hrs|	FR01|
|NFR03|	User|	Enhanced visual impact|	S|	User Impact	| |
|NFR04|	Automation|	Minimal manual input|	S|	Disruption|	|
|NFR05|	L & R|	Compliant to all L & R requirements|	M|	Legal and Regulatory|	FR01|

### Potential Extent of IT solution

### Naming Conventions
|Term| Description|
|---|---|
|TBC| TBC|
	




