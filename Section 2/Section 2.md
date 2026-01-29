**1**.
**Web Application**: The monolothic web application can be rehosted on a PaaS platform (ex: Azure App Service), whereby the application (i.e, code base, dependencies) will be uploaded to the cloud service and deployed and run on their cloud managed infrastructure. This will reduce the company's overhead of running and maintaining local servers to host the application while still being able to manage the application.

**Database**: Similarly, the on-prem database can be replatformed to a PaaS platform (ex: Azure SQL Database), reducing the company overhead of managing and maintaining their own SQL servers. Once the proper planning and setup of the cloud database has taken place, the local database can be migrated using a migration tool (ex: Azure SQL Migration), after which the data can be valaditated to ensure integrity. Considering that a company of this nature and size will likely have limited IT resources, removing the need for OS set-up, backups, redundancy, etc. can benefit the company while still allowing full control over the schema and data of the database.

**Networking/Security:** The physical on-prem networking and security, such as routers and firewalls, can be replaced by migrating these concerns to a IaaS platform (ex: Azure Firewall, Azure Virtual Network). The company will still be required to configure the virtual network and security, but concerns of managing the physical networking will be passed onto the IaaS platform.

**E-Mail Service**: The on-prem email service can be replaced using a SaaS email service (ex: Azure Communication Services). Once established, the service should provide reliable, scalable and highly available email services to for the company, eliminating the need for the direct management of any on-prem e-mail servers.

**File Storage**: The on-prem file storage solution can be replaced and migrated to a PaaS platform (ex: Azure Files). Migrating the a cloud based solution will remove the need overhead of managing a local file system while also providing built-in redundancy and scalability.

**2**.
Migrating the on-prem solutions to cloud-based solutions can be done stratigically in gradual steps via a hybrid approach to minimize the potential disturbances and pitfalls of attempting to switch over every component at once. 

**Components that can be Fully Migrated Initially:**
- **Web Application**: by initially migrating the web application to a PaaS platform, there will several immediet benefits for the company, such as built-in scaling, reduced infracture management, and high availbility. This is a fairly low risk change as the code base can remain largely unchanged, roll backs can be preformed if necessary, and the reduction of managing infracture should increase the ease of managing of the application.
- **E-Mail Service**: migrating the e-mail service to a SaaS solution should be a simple and will provide the immediet benefit of reducing the over head of managing an on-prem service. The dependencies on the e-mail service from other services is likely low, meaning the migration should have minimal impact on the running of the application. This is a low risk change as it can be easily reverted while being set-up.

**Components that can be Migrated using a Hybrid Approach:**
- **Database**: 
