Use Case 1 
===========
### Title: Check Software Package for Licenses & Vulnerabilities

Primary Actor: Developer

Goal in Context: The Developer is able to determine the license and vulnerability information in a provided software package

Stakeholders:
  * Developer: provide the software package
  * Company: approved software can be used in the company systems or sold as a product

Preconditions:
  * Relevant software information is provided
  * Developer has access to software-checking system

Main Success Scenario: Developer receives accurate license and vulnerability information for the requested software package

Failed End Connections: Developer recieves inaccurate and/or invalid license and vulnerability information for the requested
software package

Trigger: Developer uploads software package to the server to be checked 

Use Case 2
===========
### Title: Write New Policy to Policy Database

Primary Actor: Manager

Goal in Context: The Manager is able to submit new policy information to the policy database

Stakeholders:
 * Manager: provides the new policy information

Preconditions:
 * Relevant policy information is provided
 * Manager has access to policy database
 
Main Success Scenario: Manager is able to successfully write the new policy information to the policy database

Failed End Connections: 
 * Inaccurate and/or invalid policy information is written to the database
 * Policy information write fails
 
Trigger: Manager desires to add new policy information to the policy database

Use Case 3
===========
### Title: Get License & Vulnerability Information from Database

Primary Actors: Developer, Manager

Goal in Context: The Developer or Manager is able to request and receive license & vulnerability information from the database

Stakeholders:
 * Developer: license & vulnerability information may be used in the development of new software
 * Manager: license & vulnerability information may me used in writing new or modifying existing policy
 
Preconditions:
 * Manager or Developer submits request for information
 
Main Success Scenario: Manager or Developer is able to successfully retreive license & vulnerability information from the database

Failed End Connections:
 * Request for license & vulnerability information is not successfully sent
 * Invalid or inaccurate license & vulnerability information is returned
 
Trigger: Manager or Developer submits request for license & vulnerability information
