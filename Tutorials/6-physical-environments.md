## Physical environments and versioning

Now that we have a logical map of some of our Applications we can start documenting their physical deployments.  Operations, Developers, Testers and Architects are interesting in the infrastructure.

We take the previous matrix we have done and manually enter the applications, their versions, their DNS / urls.  In the future we will derive this information automatically.

#### Environment Matrix

| Application  | Local  | Development  | Test  | Quality Assurance  | Production | 
|---|---|---|---|---|--| 
| Company Website | local.company.com | dev.company.com | test.company.com | qa.company.com | www.company.com | 
| Customers API | local.customers-api.company.com | dev.customers-api.company.com | test.customers-api.company.com | qa.customers-api.company.com | customers-api.company.com | 
| Customers Database | local.customers-database.company.com | dev.customers-database.company.com | test.customers-database.company.com | qa.customers-database.company.com | customers-database.company.com |
| ... |  | |  |  |  | | 

#### Versions

| Application  | Local  | Development  | Test  | Quality Assurance  | Production | 
|---|---|---|---|---|--| 
| Company Website | 3.0.157.0 | 2.1.117.0 | 2.1.102.0 | 2.0.122.1 | 2.0.122.1 | 
| Customers API | 2.3.12.0 | 2.3.12.0 | 2.3.12.0 | 2.0.8.0 | 2.0.8.0 | 
| Customers Database | 4.2.99.4 | 4.3.1.4 | 4.1.0.1 | 4.1.0.1 | 4.1.0.1 | 
| ... |  | |  |  |  | | 

Note: DNS for databases / internal API's would only be available internally.

Physical environment documentation
Most cloud systems (Azure, AWS, Google Cloud) automatically provide an interface which describes your physical environment.  i.e all your servers, their IP addresses so it is redundant to documentat the same information.  What is important though is to map how those physical environments relate to your logical environments.  It is likely a few of your environments are breaking the rules and conventions.

#### Physical Envrionments

| Physical/Instance Environment  | Local  | Development  | Test  | Quality Assurance  | Production | 
|---|---|---|---|---|--| 
| Azure | AzureDev  | AzureSIT | AzureUAT | AzureUAT | AzureProd1, AzureDR | 
| | Local Machines |   | AWS-US-Dev02, AWS-US-Dev01(old) |  | AWS-US-Prd | 
| |  |   | Melbourne Datacenter (SIT)  |  | Melbourne Datacenter (PRD) | 