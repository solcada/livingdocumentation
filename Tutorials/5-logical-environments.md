## Environments

In most companies you have multiple different environments for the purposes of development and testing.  In an ideal world every environment has minimal deviation and propagating a feature through environments is timely.  However, most companies have budget constraints, complexity constraints and release speed constraints.  This results in the need for different environments which serve different purposes such as Quality Assurance, Integration and Development.

Here is a template for defining a few Logical environments and their purposes.

| Environment  | Local  | Development  | Test  | Quality Assurance  | Production | 
|---|---|---|---|---|--| 
| Definition | A physical or virtual machine which developers use to develop software on | A sub-set of Applications used for developing a feature | A environment which multiple teams use to integrate and test their features | A production like environment | Production (includes Disaster recovery) |
| Purpose  | Developing features | Integrating features with other components and teams  | Integrating features with other components and teams | Replicating production tests | Serving end users |
| Number of Instances  | 1> | 1> | 1> | 1 | 1 |
| Deviation from production  | Large (contains mocks, consolidated infrastructure, enabled feature toggles) | Large | Medium | Small | N/A |
| Users  | Developers | Developers and 3rd parites | Developers and Testers | Testers and the business | End Users |
| Rebuild frequency | 2 Weekly | 2 Weekly | 2 Weekly | 2 Weekly | N/A |

Note: Trunk based development and feature toggles removes the need for proliferation of environments and environment contention.

If you haven't done a excerise to define your logical environments you can use the template above.  

The importance in defining your logical environments is because by not doing it, developers, testers and the business will be tempted to utilize an environment for the wrong purpose.  Such as giving a 3rd party access to a Quality Assurance environment that has sensitive data or having a developer run 1/2 completed features against test environment introducing data corruption and false negative defects.
 
The reason these are separated from physical environments is that it is possible to have.