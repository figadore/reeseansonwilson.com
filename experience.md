## Experience and Projects

I've been passionate about web development since I worked on my first project in 2008, on an electronic RMA system to replace our existing paper-based system. Since then, I've designed and implemented multiple systems and stacks top to bottom and improved and upgraded internal tooling and processes. Some of the more notable projects include:

### Privileged Access Management (2025)
Piloted and implemented GCP's **PAM** capabilities. Normally, access to production is heavily restricted. On occasion, developers need to investigate or fix urgent issues there. I configured PAM to allow a much more streamlined method of temporarily granting elevated privileges, with the added benefit of increased visibility and auditability. 

### Security Group Automation (2025)
Designed a low-friction method of creating security groups in code. **Pulumi** parsed a yaml file with the declarative state of the groups, which then provisioned one-off groups or per-environment groups, allowing simple permissions management across microservices and decoupling of hidden deployment dependencies and start-up order.

### Internal tooling microservices (2024)
Deployed microservices to do things like track deployment status of other services across environments. Integrated with GitHub's deployments API to trigger real-time updates. Simplified the orchestration of cross-service deployments.

### Migration to fully IaC environments (2021-2023)
Moved all existing manually-created and self-hosted infrastructure and apps to new **GCP** projects using **Terraform** and **GitHub Actions**. Architected the environments and pipelines to ensure all regulatory requirements were met, favoring behind-the-scenes implementations and reduced red tape. Using the principle of "make the easy choice the right choice" to increase compliance and consistency. I developed the patterns to follow, documented everything along the way, communicated with the stakeholders to ensure all requirements were met, onboarded teams to the new environments, and followed up with additional quality-of-life improvements over time.

### Tools API (2020)
Published a public API to allow various integrations and improvements to the platform. Implemented using **API Gateway** backed by **Lambdas** and pluggable custom authorizers. This enabled everything from triggering actions based on GitHub events to automatic creation of CI namespaces. Additionally, privileged pipeline processes can now be initiated securely from the pipelines, such as using **cryptographic signatures** to verify artifact provenance and scope bounds (this was a very fun project for me).

### Migration to cloud-based tooling (2019-2020)
Moved our internal platform's build process from **Jenkins** to **CircleCI**, code from Bitbucket to Github, and artifacts from on-prem Artifactory to hosted **Artifactory**. Planned transition, set up examples to follow, created support channels and documentation, and guided developers through the migration. Our build process on Jenkins was fairly strict and locked down so that we could make certain guarantees about what was being deployed using the servers' highly privileged credentials, meaning that our team was the bottleneck whenever an update or a new feature was needed. As we moved to CircleCI, by laying a strong foundation using the **principle of least privilege**, we were able to vastly expand flexibility, empowering the development teams to help themselves, move at their own speed, and experiment in areas that we previously never would have had the bandwidth to support. Processes that previously had to be enforced at build time are now a deploy time check using the tools API I wrote.

### Developer cli (2018)
Designed a command line tool to assist developers in a variety of everyday tasks, from promoting a build to validating a config against a schema. Innersource: it was created to maximize ease of contribution, which was a key factor in its success and adoption. The modular architecture allows contributors to drop in their own functionality in new commands in any language with only minor wiring to hook into the wrapper's help docs. It is cross-platform, self updating and is automatically versioned (at least for minor and patch releases).

### Platform upgrade (2017-2019)
Our internal platform enables developers to specify the infrastructure and resources they need for their microservices and serverless stacks using a custom DSL and convention over configuration to produce and deploy mostly **CloudFormation** templates, abstracting away most of the nuances and gotchas of that arcane field. This project involved taking the existing platform and bringing it to the next level as far as features, maintainability, community and ease of contributions, consistency, and overall polish. The original code base was a large **Python** script that had to be refactored in a backwards compatible way, so the first thing added was a suite of tests that ensured the outputs would remain the same throughout the rework. This also made it possible to receive contributions without fear of the domino effect or hidden side effects. Hand-crafted and maintained **Jenkins** jobs were converted to code using the **groovy** DSL making it easy to roll out changes to everyone at once. Portability was important, so the process was **dockerized**, relieving us from the pressures of relying on incompatible Jenkins plugins and other environment dependencies. Deployments were parallelized by creating a **Codepipeline** and **Codebuild** for each project, eliminating long wait times and allowing canary-style pipeline development. Documentation was added throughout, and channels for getting help were created. Additionally, a community was fostered so that support was eventually mostly self-sustaining. By the end of the project the platform was considered more stable and understandable, and developers had consistent builds and confidence in the quality of their contributions.

### **Heart Monitor** (2010-2012)
Part of a team of three inexperienced engineers who designed an internet-connected portable heart monitor from scratch, got it through FDA approval, worked with manufacturers, and supported the device as it was sold. Wrote **HTTP** stack for an embedded system (**C++**), replacing FTP implementation from our prototype, and vastly improving potential for server-side capabilities. I also wrote the code for the UI, designed the label and menu graphics, and did the mechanical engineering and design.

### Heart monitor report generating software (2015-2017)
Designed and developed a HIPAA compliant system for managing cardiac studies, including ability for technicians to generate reports for doctors. Integrates with EMRs for managing patients and facilities. Microservice based architecture using **hypermedia REST APIs** and **JSON schema**. Uses **Docker** containers for microservices. Deployed to AWS with **Kubernetes**. Logging and monitoring are done with the help of **Elasticsearch** and **Kibana**. Written mostly in **Node.js** and **Express**. **Drone CI** system for automated image building and **unit/integration tests** (using **mocha**, **karma**, **selenium** and **protractor**)

### Heart monitor incoming file processing (2014)
Designed and developed a low-level service layer for managing the device side of cardiac studies. Processes incoming files from devices, runs them through an algorithm for additional arrhythmia detection. Written in PHP ( **ZF2**), stores files in **S3** through an abstracted key-value data store layer. Provides a **REST API** for third party developers. Unit tested with **PHPUnit**. Deployed to EC2 using Chef. Later **Dockerized** and deployed with **Kubernetes**. Also uses **jQuery** and **Bootstrap** 

### Heart monitor device management (2013)
Designed and developed a system for managing inventory of devices, including serialization, assignment to customers, wireless settings programming, and automated SMS sending to initiate device actions. Uses PHP (**ZF2**) and MySQL on the backend, **jQuery** and **SASS** on the frontend, deployed to **EC2** and **RDS**

### Monitor interactions (2012)
Designed and developed a server that interacts with the portable heart monitors' HTTP stack to send and receive files during setup and operation. Uses PHP to perform low-level file parsing and composing, deployed to **AWS EC2** with **Chef**. Uses **Zend Framework**

### CRM (2010)
Designed and developed a CRM that integrates with our internal sales database and Google Apps to provide sales team with all the tools they need to manage their sales pipelines. Migrated data from pricey, bloated legacy CRM. Uses **CakePHP**, **Javascript** ( **jQuery** ) and **MySQL**, authenticates with **OpenID**, deployed on-premise with **Chef**

### DMS (2009)
Installed DMS from the market to migrate our paper document management to an electronic system. Wrote **PHP** plugins to customize the behavior to be compatible with regulatory document control requirements

### Sales database and commissions reports (2008)
Integrates with accounting system to inform our sales team about historical sales and their current commissions. **ASP.net** backend, uses complex **MySQL** queries and stored procedures extensively, works with Active Directory for integrated authentication on Windows

### Other

Side projects have also resulted in experience with **Go**, **Typescript**, graph databases (**neo4j**, **cypher**) and **Java** (**Android**), as well as tools for other fields such as **SolidWorks**, **Blender**, **Photoshop**, **Illustrator**
