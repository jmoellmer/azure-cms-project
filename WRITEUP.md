# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

For a Virtual Machine (VM) solution, there are lower up-front costs compared to purchasing and maitaining on-premise hardware. Additionally, there are multiple types of hardware configurations, allowing you to pay only for what meets your needs. Additional expenses are also incured due to time spent by developers compared to App Services. In general, compared to an App Service Solution, VMs are more expensive.

For VMs, there are two scaling options--VM Scale Sets and Load Balancers. These allow multiple VMs to be gropus to provide high availability, scalability, and redundancy. However, you will pay for additional VMs used in these solutions, which increases cost. App Services also includes scaling features: Vertical or Horizontal scaling. App Services has high availability, auto scaling, and the offers lowering costs by using a Linux enviroment intead of a Windows one. 

In terms of workflow, VMs provide Infrastructure as a service (IaaS), requiring developers to use Azure to design, create, and setup the entire infrasturcutre themselves. This can be more time consuing for the developer than other compute options. App Services, on the other hand, is a Platform as a Service (PaaS) offering, which allows a developer to foucse ont he application while Azure takes care of the infrastructione.

For this project, the appropriate solution is the App Service. I do not need control of the underlying operating system and I am not using custom software to support my needs. We are using Python and Flask, which is supported as a language and web framework in an Azure PaaS offering. Also, this Flask web application is light weight and fits within the hardware limitations of an App Service (14GB RAM and 4 vCPUs per instance).

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

If I wasn't using Python and Flask, but instead a web framework that was a supported language of the App Service, I would need to use a VM. Another consideration that would affect the decision is if we needed to control of the underlying operating system or needed to install custom software to support the applicaiton. Finally, if the web application needed more RAM and vCPUs per instance, then it wouldn't fit within the App Service model today, and VMs would need to be used.