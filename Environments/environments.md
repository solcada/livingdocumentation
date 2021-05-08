# Environments
 
 | Environment  | Local  | Development  | Test  | Quality Assurance  | Production | 
|---|---|---|---|---|--| 
| Definition | A physical or virtual machine which developers use to develop software on | A sub-set of Applications used for developing a feature | A environment which multiple teams use to integrate and test their features | A production like environment | Production (includes Disaster recovery) |
| Purpose  | Developing features | Integrating features with other components and teams  | Integrating features with other components and teams | Replicating production tests | Serving end users |
| Number of Instances  | 1> | 1> | 1> | 1 | 1 |
| Deviation from production  | Large (contains mocks, consolidated infrastructure, enabled feature toggles) | Large | Medium | Small | N/A |
| Users  | Developers | Developers and 3rd parites | Developers and Testers | Testers and the business | End Users |
| Rebuild frequency | 2 Weekly | 2 Weekly | 2 Weekly | 2 Weekly | N/A |