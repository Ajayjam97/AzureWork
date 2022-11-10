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
<ul>
 <li>Virtual Machines</li> 
 Provides a virtual server running on a physical server by utilizing physical hardware and sharing resources using virtualization. It is a regular server that can be accessed using RDP or SSH protocols. Virtual machines can be created using below steps: <br>
 1. Go to pricing calculator & add a VM. Check the price it is taking. <br>
 2. To create a VM in Azure navigate to Home > Virtual machine <br>
 3. 
 
 <li>App Services</li>
 <li>AKS</li>
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
 </ol>

 </details>
