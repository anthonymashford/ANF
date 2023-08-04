# Azure NetApp Files Proof of Concept Planner

### Document Purpose

The purpose of this document is to assist with the planning of a Proof of Concept (PoC) of **Microsoft** Azure NetApp Files. It has been produced as a guide to enable a successful deployment, test and validation of the service.

### In this doucment you will find the following sections:
<a name="Considerations"></a>[Considerations](#Considerations)<br>
<a name="Test"></a>[Test Data Preparation](#Test)<br>
<a name="Workload"></a>[Workload Configuration](#Workload)<br>
<a name="Performance"></a>[Performance Testing](#Performance)<br>
<a name="FeatureTesting"></a>[ANF Feature Testing](#FeatureTesting)<br>
<a name="Documentation"></a>[Documentation and Reporting](#Documentation)<br>
<a name="Architectures"></a>[Azure NetApp Files Solutions Architects](#Architectures)<br>
<a name="ANFfaq"></a>[Azure NetApp Files FAQ](#ANFfaq)<br>
<a name="PoCWorkflow"></a>[Example: Proof of Concept Workflow](#PoCWorkflow)<br>


<p id="Considerations"></p>

## Considerations

The following is a list of prerequisites & considersations required to support the Proof of Concept (PoC) for testing and validating Azure NetApp Files:

### Objectives and Requirements:
- Clearly define the objectives of the PoC, such as functional testing, performance and scalability, backup and disaster recovery requirements
- Identify the workload(s) to be tested, such as SAP, AVS, HPC, AVD, Oracle, SQL or Enterprise File Shares.

### Stakeholders:
- Identify key stakeholders. These are teams or staff members required to support the PoC, such as, storage teams, networking teams, active directory teams, application owners, cloud platform teams.

### Azure Subscription(s):
- An Azure subscription is required to create and manage Azure resources.

### Geographical location(s):
- Define the Azure Region(s) where the PoC will be deployed. 

### Virtual Network (VNet):
- A Virtual Network (VNet) in Azure to provide network connectivity for your resources.

### Subnet:
- A subnet within the VNet delegated to the Azure NetApp Files service.
  
### Authentication (Active Directory):
- The creation of SMB volumes requires an Active Directory (AD) domain or Azure Active Directory Domain Services (AADDS).
- Ideally a domain controller in the same region as the Azure NetApp Files volumes. This can be an existing domain controller or a new one created for the PoC.
- The domain controller must be accessible from the Azure NetApp Files subnet.

### Azure NetApp Files Account(s):
- An Azure NetApp Files account in your Azure subscription. This account will serve as the logical container for your Azure NetApp Files resources.

### Azure NetApp Files Capacity Pool:
- A Capacity Pool within your Azure NetApp Files account. Capacity Pools provide a way to manage and allocate storage capacity for your Azure NetApp Files volumes.

### Azure NetApp Files Volumes: 
- One or more Azure NetApp Files volumes within your Capacity Pool. These volumes will be used to store your data and will be the target of your testing and validation.

### Workload Generation Tools:
- Identify and prepare the necessary workload generation tools or scripts to generate the desired workload on the Azure NetApp Files volumes. This could include tools specific to your workload type or general-purpose load testing tools.

### Test Data: 
- Gather or generate representative test data that aligns with your workload characteristics. This data should be ready for upload or use during the PoC.

### Virtual Machines (VMs): 
- Prepare the necessary Virtual Machines (VMs) to host the workload. Ensure that these resources are properly configured, including network connectivity to the Azure NetApp Files volumes.

### Monitoring and Performance Measurement:
- Determine the metrics you want to monitor and measure during the PoC, such as IOPS, throughput, and latency. Set up the appropriate monitoring tools to capture and analyse these metrics.

### Documentation and Reporting:
- Document the PoC setup, configuration, test results, and observations. Define the structure for your final PoC report, including sections for objectives, methodology, results, and conclusions.

<p id="Test"></p>

## Test Data Preparation:
- Generate or gather representative test data for your workload.
- Determine the size and characteristics of the data required for testing.
- Prepare the test data and ensure it's ready for use.

<p id="Workload"></p>

## Workload Configuration:
- Determine the workload characteristics you want to test, such as IOPS, throughput, latency, and concurrency.
- Configure the virtual machines (VMs) or other infrastructure to host the desired workload.
- Install and configure any necessary software or tools required.

<p id="Performance"></p>

## Performance Testing:
- Start the workload generation tools and configure them to target the Azure NetApp Files volumes.
- Monitor and measure key performance metrics, such as IOPS, throughput, and latency.
- Gradually increase the workload to assess the scalability and performance limits of Azure NetApp Files.
- Analyse the performance data and compare it against your requirements and expectations.

## Feature Testing:

<p id="FeatureTesting"></p>

- Explore and test advanced features of Azure NetApp Files, such as snapshotting, cloning, replication and backup.
- Validate the behaviour and performance of these features in your specific use cases.
- Test any integration points with other Azure services or applications.

<p id="Monitoring"></p>

## Monitoring:
Enable monitoring of the Azure NetApp Files service using the Azure Portal, Azure Monitor and Azure NetApp Files Metrics. Below are links to the Azure NetApp Files documentation for monitoring. 
- <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/monitor-azure-netapp-files' target='_blank'> Monitoring Azure NetApp Files</a>
- <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-metrics' target='_blank'> Metrics for Azure NetApp Files</a>

<p id="Documentation"></p>

## Documentation of the PoC:
- Document the entire PoC process, including the setup, configuration, and test results.
- Summarise the findings and observations from each test scenario.
- Provide recommendations and insights based on the results.
- Create a comprehensive report that includes the objectives, methodology, results, and conclusions of the PoC.

<p id="Architectures"></p>

## Azure NetApp Files Solutions Architects:
Below is a link to the Azure NetApp Files Solution Architectures page. This page contains a list of solution architectures that have been tested and validated by the Azure NetApp Files team. These architectures can be used as a reference for your PoC.
- <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-solution-architectures' target='_blank'> Azure NetApp Files Solution Architectures</a>

Remember to follow best practices, consult Azure NetApp Files documentation, and engage with the NetApp Azure CSA team during the PoC.

<p id="ANFfaq"></p>

## Azure NetApp Files FAQ:
Below is a link to the Azure NetApp Files FAQ page. This page contains a list of frequently asked questions and answers about Azure NetApp Files.
- <a href='https://docs.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-faqs' target='_blank'> Azure NetApp Files FAQ</a>

<p id="PoCWorkflow"></p>

## Example: Proof of Concept Workflow
Below is a recommended workflow to follow to for Azure NetApp Files PoC.

**Note:** The following workflow is a guide only and may not be suitable for all PoC scenarios.

### Creation of the PoC Environment:
- It's important to review the Azure NetApp Files documentation and best practices to ensure a smooth implementation of the PoC and to address any additional prerequisites specific to your use case.

- Create an Azure subscription or use an existing one.

- Allocate permissions using Role Based Access Control (RBAC) to users required to interact with the service.

- Select the region or regions where the PoC needs to run. Regional availability can be found here: <a href='https://azure.microsoft.com/en-gb/explore/global-infrastructure/products-by-region/?products=netapp&rar=true&regions=all' target='_blank'> ANF Regional Availability</a>
- Register the ANF resource provider within the chosen subscription(s). Details here <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-register' target='_blank'> Register ANF Resource Provider</a>
- Configure Azure networking. Utilise existing or create a Virtual Network (VNet) and delegated subnet. Link here <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-delegate-subnet' target='_blank'> Configure Azure networking for Azure NetApp Files</a>
- Provision an Azure NetApp Files account in your chosen region(s). Link here <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-create-netapp-account' target='_blank'> Create an Azure NetApp Files account</a>
- Configure Active Directory connection (optional, but required for SMB volumes). Link here <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/create-active-directory-connections' target='_blank'> Create Active Directory connections</a>
- Create capacity pool(s) as required. Link here <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-set-up-capacity-pool' target='_blank'> Create capacity pools</a>
- Deploy Azure NetApp Files volume(s) based on your requirements. Assoicated links below:
    - <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-create-volumes' target='_blank'> Create NFS volume</a>
    - <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb' target='_blank'> Create SMB volume</a>
    - <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/create-volumes-dual-protocol' target='_blank'> Create dual protocol volume</a>
- Mount the volumes on the required VMs. Links below:
    - <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-mount-unmount-volumes-for-virtual-machines#mount-nfs-volumes-on-linux-clients' target='_blank'> Mount NFS volume</a>
    - <a href='https://learn.microsoft.com/en-us/azure/azure-netapp-files/mount-volumes-vms-smb' target='_blank'> Mount SMB volume</a>
