**1**.
**Web Application**: The monolithic web application can be rehosted on a PaaS platform (ex: Azure App Service), whereby the application (i.e, code base, dependencies) will be uploaded to the cloud service and deployed and run on their cloud managed infrastructure. This will reduce the company's overhead of running and maintaining local servers to host the application while still being able to manage the application.

**Database**: Similarly, the on-prem database can be replatformed to a PaaS platform (ex: Azure SQL Database), reducing the company's overhead of managing and maintaining their own SQL servers. Once the proper planning and setup of the cloud database has taken place, the local database can be migrated using a migration tool (ex: Azure SQL Migration), after which the data can be validitated to ensure integrity. Considering that a company of this nature and size will likely have limited IT resources, removing the need for OS set-up, backups, redundancy, etc. can benefit the company while still allowing full control over the schema and data of the database.

**Networking/Security:** The physical on-prem networking and security, such as routers and firewalls, can be replaced by migrating these concerns to a IaaS platform (ex: Azure Firewall, Azure Virtual Network). The company will still be required to configure the virtual network and security, but concerns of managing the physical networking will be passed onto the IaaS platform.

**E-Mail Service**: The on-prem email service can be replaced using a SaaS email service (ex: Azure Communication Services). Once established, the service should provide reliable, scalable and highly available email services for the company, eliminating the need for the direct management of any on-prem e-mail servers.

**File Storage**: The on-prem file storage solution can be replaced and migrated to a PaaS platform (ex: Azure Files). Migrating to a cloud based solution will remove the overhead of managing a local file system while also providing built-in redundancy and scalability.

**2/3**.
Migrating the on-prem solutions to cloud-based solutions can be done strategically in gradual steps via a hybrid approach to minimize the potential disturbances and pitfalls of attempting to switch over every component at once. This approach can be used as migration plan for company to shift their services to the cloud.

**Components that can be Fully Migrated Initially:**

- **Networking/Security**: initially moving the networking and security to a IaaS platform is likely a good idea for a couple reasons. Networking provides the foundation for how the different services will communicate with eachother. Without networking in place early on, the web application won't be reachable, nor will it be able to communicate with the database. Moving the security to an IaaS platform early on is also sensible, as setting up cloud based security first ensures that traffic is properly controlled and secured before any application workloads are migrated. These should be a low risk endeavors as no production systems need to be modified (i.e, data, application logic) and it can be tested in isolation.

- **Web Application**: initially migrating the web application by rehosting it to a PaaS platform, can provide several immediate benefits for the company, such as built-in scaling, reduced infrastructure management, and high availability. This is a fairly low risk change as the code base can remain largely unchanged, rollbacks can be preformed if necessary, and the reduction of managing infrastructure should increase the ease of managing of the application.

- **E-Mail Service**: moving the e-mail service to a SaaS solution should be a simple and will provide the immediate benefit of reducing the over head of managing an on-prem service. The dependencies on the e-mail service from other services is likely low, meaning the change should have minimal impact on the running of the application. This is a low risk change as it can be easily reverted while being set-up.


**Components that can be Migrated using a Hybrid Approach:**

- **Database**: since the database is likely tightly coupled to the application, initially moving it to a IaaS platform may prove prudent, as full control over the environment (i.e, OS) and the database (i.e, SQL version) can be retained. Immediate changes to the environment (i.e, moving to a PaaS platform) may require redesigns of the database to be compatible with the PaaS database solution, which may be more challenging and error prone than using a lift and shift approach to a IaaS platform.

- **File Storage**: the file system can initially remain on-prem while other services are moved to cloud solutions, in order to reduce the impact and potential pitfalls of migrating all aspects of the application in one go. Once the above components of the system are migrated to the cloud, the file system can be moved to an IaaS platform using a lift and shift approach to minimize the likelihood of misintegration challenges.
