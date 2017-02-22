## Entities:

  * Developer: creates software for the company

  * Manager: oversees the deparment in which he/she works

## Processes:

 * Scan for Licenses: software sent to this process is read to see if it contains any licenses, then is sent back to "Check Software"

 * Check Software: this process acts as a hub process, redirecting information it receives based on what it is and where it comes from:
 
 | Receives | From | Sends To |
 | -------- | ---- | -------- |
 | Software Package | Developer | Scan for Licenses, NIST Vulnerability Database |
 | Software Licenses | Scan for Licenses | Developer, License & Vulnerability Database (in Software Scan Results) |
 | Software Vulnerabilities | NIST Vulnerability Database | Developer, License & Vulnerability Database (in Software scan Results |

 * Retrieve L&V Information: receives a request for license and vulnerabilites from either the develoer or manager, queries the
   License & Vulnerability Database, and sends the results back to whichever entity submitted the request

 * Write Policy: receives a new policy document and writes it to the Policy Database

 * Modify Existing Policy: receives a request for existing, queries the Policy Database for it, and sends it back to the Manager.
   Then receives a modified policy document from the Manager and writes it to the policy database

 * Compare Package: recieves a project request from the Manager and compares it to existing policy in the Policy Database, then
   sends the results back to the Manager

## Data Repositories:

 * NIST Vulnerability Database: National known vulnerability database

 * License & Vulnerability Database: company database containing license & vulnerability information on company software

 * Policy Database: company database containing policy documents

## Data Flows:

 * Software Package: software created by the Developer

 * Software Licenses: Licenses detected in Software Package by Scan for Licenses

 * Software Scan Results: combination of Software Licenses and Software Vulnerabilities

 * Software Vulnerabilities: Vulnerabilities detected in Software Package

 * L&V Results: License & Vulnerability information requested from License & Vulnerability Database by Manager or Developer

 * Request L&V: Request for License & Vulnerability information from Developer or Manager

 * Policy Package: Policy document being submitted to or retreived from Policy Database

 * Request Policy: Request sent by Manager for existing policy document in Policy Database

 * Modified Policy: Existing policy that has been edited/changed by Manager

 * Project Request: collection of software documents submitted by Manager to be checked against the Policy Database

 * PR Results: Results of existing policy being compared to Project Request

 * Policy Results: Existing Policy that applies to Project Request
