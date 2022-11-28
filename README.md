# AzureWork


## Understanding cloud & Azure

<br>

<details>
<summary>What is cloud?</summary>

Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking. There are many other new & hybrid services as well.
Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking. Cloud computing falls under OpEx because cloud computing operates on a consumption-based model.
<ul>
 <li>Cloud Model types <br>
  Public: (Azure, AWS, GCP)  <br>
  Private: (VMWare, RedHat OpenShift, Azure Stack) <br>
  Hybrid: (Azure Arc, AWS Outposts)
 </li>
 <li>Cloud Service types (IAAS, PAAS, SAAS)</li>
 </ul>

</details>

<details>
<summary>Intro to Azure</summary>
Azure is the public cloud offering from Microsoft. It provides more than 100 services that enable you to do everything from running your existing applications on virtual machines to exploring new software tools & services (Containerization, Blockchain, ML, AI, IOT etc). <br> <br>
As cloud is just another computer that multiple users are accessing through the internet. Cloud vendors make use of economies of scale & global reach to profit through their online computing services. Azure has the biggest set of data centers(Zones) spread across Regions which are further part of different geographies across the Globe. <br> <br>
Find the latest Global infrastructure of Azure below. <br> 
https://infrastructuremap.microsoft.com/explore <br> <br>
A list of all cloud services provided by Azure can be found below. <br>
https://azure.microsoft.com/en-in/products/ 
<br>
 
</details>

<details>
<summary>A look at Azure</summary>
To create and use Azure services, you need an Azure subscription. After you've created an Azure account, you're free to create additional subscriptions. After you've created an Azure subscription, you can start creating Azure resources within each subscription. Creation of resources & other operations can also be performed either from the Azure Cloud Shell on the portal or you can download it to your local. Portal can be accessed from below link. <br>
https://www.portal.azure.com
<br>
 
</details>

<details>
<summary>Basics of Azure</summary>
The physical infrastructure for Azure starts with datacenters. Conceptually, the datacenters are the same as large corporate datacenters. They’re facilities with resources arranged in racks, with dedicated power, cooling, and networking infrastructure. <br>
 
As a global cloud provider, Azure has datacenters around the world. However, these individual datacenters aren’t directly accessible. Datacenters are grouped into Azure Regions or Azure Availability Zones that are designed to help you achieve resiliency and reliability for your business-critical workloads. <br>
 
A region is a geographical area on the planet that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network. When you deploy a resource in Azure, you'll often need to choose the region where you want your resource deployed. <br>
 
You can use availability zones to run mission-critical applications and build high-availability into your application architecture by co-locating your compute, storage, networking, and data resources within an availability zone and replicating in other availability zones. Keep in mind that there could be a cost to duplicating your services and transferring data between availability zones. <br>
 
Also, most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This approach allows for the replication of resources across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect an entire region.
</details>
<br>

## Main services in Azure

<br>

<details>
<summary>Compute Services</summary>
<ul> <br>
 <li>Virtual Machines</li> 
 Provides a virtual server running on a physical server by utilizing physical hardware and sharing resources using virtualization. It is a regular server that can be accessed using RDP or SSH protocols. Virtual machines can be created using below steps: <br> <br>
 
 1. Go to pricing calculator & add a VM. Check the price it is taking. <br>
 2. To create a VM in Azure navigate to Home > Virtual machine <br>
 3. After creating VM you can connect to it using RDP or SSH thorugh its public IP. <br>
 4. Even after the VM is stopped, it keeps on incurring cost due to resources (Disk, IP, Storage). <br>
 5. Thus the reosurce group / all the resources of VM need to be deleted to prevent cost consumption. <br>
 6. Ways to reduce VM costs (Auto shutdown, Reserved Instance, Spot Instances, Disk optimization). <br>
 7. While creating the VM make sure to configure it for high availability, low cost consumption & download its ARM template. <br>
 8. An ARM template is a JSON file that can be exported, modified, uploaded & deployed. <br>
 9. If you run Azure Cloud Shell, a storage account under a default resource group would get created for cloud shell. <br>
 10. Upload your ARM templates to the file share of cloud shell & run command "az deployment group create --resource-group First-rg --template-file template.json --parameters parameters.json" inside the folder in cloud shell. <br>
 11. VM scale set is a group of seperate VMs sharing the same image. They can be used with load balancers to handle unpredictable load.<br>
 12. Shutdown the VMs when not in use.<br> <br>
 
 <li>App Services</li>
 App Services provide a fully managed web hosting for websites. Microsoft manages the hosting & security for the hosted application. We just need to publish and run the app service. There is no access to the underlying servers. App service integrates with many source control & devops engine. It supports platforms like .NET, Nodejs, PHP, Java, Python etc. It can host web apps, web apis & web jobs. It is extremely easy to deploy. <br> <br>
 
 1. Check the pricing for the app service at https://azure.microsoft.com/en-us/pricing/details/app-service/windows/#pricing <br>
 2. To create App Service in Azure navigate to Home > App Service <br>
 3. After creating the app service, the published files can be deployed and the working application can be accessed from url.<br>
 4. Go to VS Code & use command "dotnet publish -o publish". Right click on the publish folder select deploy to Web App. This option is present due to Azure Web App       extension. <br>
 5. After deployment, the app service files can be modified & managed from console, App Service Editor.<br>
 6. By default, App Services can be accessed using http and https. You can make it https only in the TLS/SSL settings in the App Service menu. <br>
 7. App service can also run batch processes, or continuous jobs, with the request/response  paradigm. This can be done using the WebJobs menu item, where you can upload exe file that will run always, or on scheduled times. <br>
 8. You can find there the Virtual IP address of the App Service, and also - the Outbound IP addresses in gthe properties page. <br>
 9. While you can stop an App Service (using the Stop button at the top of the Overview page), all it will do is to stop the functionality of the App Service, but you'll still pay for it. <br>
 10. With VM - you pay only when the VM is On. With App Service - The only way to stop paying for it is to completely delete it. <br> <br>
 
 
 <li>AKS</li>
 Azure Kubernetes services is used as a managed Kubernetes on Azure. It allows deploying containers & managing them using Kubernetes on Azure. We pay only for the instances(VMs) used by Kubernetes. Containers are like thin packaging models which packages software, its dependencies & configuration files. They provide better performance, predictibility & density in deployment. Containers share the same OS, so isolation is less as compared to VM. Docker is the most popular container environment. Docker architecture consists of Docker Host & Registery. The Docker host contains daemon/server which turns containers on/off, tracks activity, build containers based on images & exposes API for management. The Docker Registery is a repository of the images used by Docker Host. For managing deployment, scalability, monitoring, routing & high-availability of contianers we use container management tools like Kubernetes.
 <br> <br>
 
 1. Installing Docker. https://docs.docker.com/desktop/install/windows-install/<br>
 2.  <br>
 3. <br>
 4.  <br>
 5. <br>
 
 
 <li>Azure Functions</li>
 </ul>
</details>

<details>
<summary>Networking Services</summary>
<br>
 
</details>

<details>
<summary>Database & Storage Services</summary>
<br>
 
</details>

<details>
<summary>Messaging Services</summary>
<br>
 
</details>


<details>
<summary>Azure Active Directory</summary>
<br>
 
</details>


<details>
<summary>Monitoring in Azure</summary>
<br>
 
</details>


<details>
<summary>Security in Azure</summary>
<br>
 
</details>


<details>
<summary>Disaster Recovery in Azure</summary>
<br>
 
</details>

<details>
<summary>Managing Costs</summary>
 
Almost everything in the cloud costs money. Cloud has below pricing models:
 <ul>
 <li>Per resource (VMs)</li>
 <li>Per consumption (Function apps)</li>
 <li>Reservations (Reserved instances)</li>
  </ul>
  Before allocating resources,always calculate their prices in pricing calculator.
  https://azure.microsoft.com/en-in/pricing/calculator/ 
  <br>
To do budgeting in Azure navigate to
Home > Cost Management + Billing  > Cost Management > Budgets <br>
Here you can describe your Annual/Monthly budget & can set alerts based on the threshold of thebudget.
 
<br>
 
</details>

<details>
<summary>Azure Policy</summary>
<br>
 
</details>


<br>

## Archetecting modern apps in Azure


<details>
<summary>Setting up development environment</summary>
 
 <ol>
 <li>Install .NET SDK</li>
 <li>Install VS Code</li>
 <li>Install extensions, Azure account & Azure App Services</li>
 <li>Use command dotnet run to run the application on localhost</li>
 <li>Use command dotnet publish -o publish to publish the application</li>
 <li>To set up IIS server connect to Windows VM using RDP. Using server manager dashboard in server roles install "Web Server (IIS)". Also install dotnet hosting bundle to host dotnet applications. Publish your application and add site in IIS.</li>
 <li>To set up linux server connect to Ubuntu VM using SSH(Putty). Use command "Sudo apt install git", "Sudo apt update", "Sudo apt install nodejs". Git clone the api to be hosted & use command "sudo apt install npm", "npm start".</li>
 </ol>

 </details>
