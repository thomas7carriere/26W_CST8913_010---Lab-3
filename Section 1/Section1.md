<img width="877" height="952" alt="image" src="https://github.com/user-attachments/assets/c91c04c8-d0ab-4084-a24c-ee2f47c9eba2" />

**Web Application**: The web application could be migrated to either a IaaS or a PaaS solution. Given that the company is mid-sized and a non-technical company, IT resources are most likely sparse. This would make migration to a IaaS platform difficult as the additional set-up and responsibility may prove difficult for a company without the proper expertise. A better approach would be to use a PaaS platform as many aspects of the infrastructure will be managed for the company. 

**Database**: Assuming a retail company of this size does not government regulations mandating data be stored on-prem, there is no need for the SQL server to be hosted by the company. By migrating to a PaaS platform, several aspects of the database will be managed for the company (i.e OS, runtime, patching), with the company still being responsible for the schema and data.

**Networking/Security**: These concern can be migrated to a IaaS platform, (ex: Azure Firewall and Azure Virtual Network). The platform will provide the hardware and management of the physical infrastructure; however, the company would still be required to configure the network and security.

**E-Mail Service**: the on-prem E-mail server is uncessary overhead given the nature of the company. There are many SaaS e-mail services that will provide scaling, high-availibity and reliability for the company without them having the run their own local e-mail server. Amazon SES is an example of such as service.

**File Storage**: Similarly, the on-prem file storage solution is uncessary overhead for the company. Moving this service to PaaS platform (ex: Azure Files) will provide the company with a robust cloud file system without the company having to manage aspects such as redundancy, scalability and security.
