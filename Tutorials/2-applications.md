## Application inventory

### Defining your applications
We are going to define an Application as something which is running in an environment and can be packaged and versioned.  

For example your organizations website, its API's, its intranet.  Don't worry if you get this wrong, Living Documentation is iterative and we will add more criteria to help define what an Application is.

Start anywhere and capture a list of Applications at your organisation.
- Company Website
- Payments API
- Customers API
- Products API

We are not defining as an application are 
- Things which are not installed or actively running (i.e software sitting on a shelf)
- Commodity software which has not been modified (e.g Microsoft word, excel).  This is noise which can be captured in a CMDB.

Once we have a rough list of your companies application, we will create pages for them under an Applications section.

Each page should contain the following, which we will add to

#### Overview 
A description of the Application which contains a business defintion so that it is useful for all audiences.

#### Used by
A link to other Application pages which consume this application.  e.g Customers API is used by the Company Website

#### Depends On
A link to other Application pages which this application depends on.  e.g Company Website depends on the Customer API

#### Source Control
A link to the source control repository of this application.

Repeat step 1 with every important application you interact with and this will build up a graph of dependencies within your organisation.  This is called discoverable documentation.  You can land anywhere in the organisations graph and have visibility of the dependencies between applications.

The rule is, if something is significant then document it, if it is not significant, dont.