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

NIST Vulnerability Database:

License & Vulnerability Database:

Policy Database:

## Data Flows:

Software Package:

Software Licenses:

Software Scan Results:

Software Vulnerabilities:

L&V Results:

Request L&V:

Policy Package:

Request Policy:

Modified Policy:

Project Request:

PR Results:

Policy Results:
