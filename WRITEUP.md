# Write-up App Service vs. Virtual Machine

## Analyze, choose, and justify the appropriate resource option for deploying the app.

### Virtual Machine:
- costs: Virtual Machines are generally more expensive than Azure App Services (at least when they are running permanently).
- scalability: Virtual Machines offer high scalability since you can group several VMs and there are many different types and sizes.
- availablility: To grant a high availablility VMs need much attention for setting them up correctly (e. g. using load balancing) and for maintainance since you take full charge of the operating system.
- workflow: You can install custom images on VMs.

### App Service:
- costs: You’re always paying for the service plan, even if your services or application isn’t running.
- scalability: Vertical and horizontal scaling is possible, even there are some hardware limitations. 
- availablility: Depending on the service plan App Services offer a high availability with less effort.
- workflow: Continuous deployment model using GitHub, Azure DevOps, or any Git repo is possible.

### Choice: App Service

Since the website should be continiously running a the PaaS "App Service" is the cheaper choice. Also a high availablility is granted by the App Service with less effort and we can therefore concentrate more on improving the app. The continuos deployment model makes such improvements even easier. Moreover the limitations regarding the scalablility don't bother since the options for the App Service are more than enough. We also don't need the control of the operating system since we need no special applications within the webapp. In my opinion the App Service is therefore the better choice for the Service

## Assess app changes that would change your decision.

When there are ne requirements regarding the security of the application (e. g. if some articles needs to be stored seperately for confidentaly reasons) or if specific applications which don't run on an App Service needs to be integrated (e. g. an already existing C# implemented search engine should be integrated) a VM would make more sence. Also if the CMS grows so big that the maximal sizes for the App Service aren't enough anymore the switch to VMs would be necessary.