# Azure NetApp Files Proof of Concept Planner

The purpose of this document of assist with the planning of a Proof of Concept (PoC) for the Azure NetApp Files service.

It has been produced as a guide to enable a successful deployment, test and validation of the service.

## Prerequisites & Required Resources

The following is a list of prerequisites required to support the Proof of Concept (PoC) for testing and validating Azure NetApp Files:

**Define Objectives and Requirements:**
- Clearly define the objectives of the PoC, such as functional testing, performance and scalability, backup and disaster recovery requirements
- Identify the workload(s) to be tested, such as SAP, AVS, HPC, AVD or enterprise file shares.

**Stakeholders:**
- Identified key stakeholders. These are teams or staff members required to support the PoC, such as, storage teams, networking teams, active directory teams, application owners, Azure/Cloud platform teams.

**Azure Subscription:**
- To support the PoC, an Azure subscription is required to create and manage Azure resources.

**Geographical location(s):**
- Define the Azure Region(s) required to support the PoC.

**Virtual Network (VNet):**
- A Virtual Network (VNet) in Azure to provide network connectivity for your resources.

**Subnet:**
- A subnet within the VNet delegated to the Azure NetApp Files service.

**Azure NetApp Files Account(s):**
- An Azure NetApp Files account in your Azure subscription. This account will serve as the logical container for your Azure NetApp Files resources.

**Azure NetApp Files Capacity Pool:**
- A Capacity Pool within your Azure NetApp Files account. Capacity Pools provide a way to manage and allocate storage capacity for your Azure NetApp Files volumes.

**Azure NetApp Files Volumes:** 
- One or more Azure NetApp Files volumes within your Capacity Pool. These volumes will be used to store your data and will be the target of your testing and validation.

**Workload Generation Tools:**
- Identify and prepare the necessary workload generation tools or scripts to generate the desired workload on the Azure NetApp Files volumes. This could include tools specific to your workload type or general-purpose load testing tools.

**Test Data:** 
- Gather or generate representative test data that aligns with your workload characteristics. This data should be ready for upload or use during the PoC.

**Virtual Machines (VMs) or Infrastructure:** 
- Prepare the necessary VMs or infrastructure to generate the workload. Ensure that these resources are properly configured, including network connectivity to the Azure NetApp Files volumes.

**Monitoring and Performance Measurement:**
- Determine the metrics you want to monitor and measure during the PoC, such as IOPS, throughput, and latency. Set up the appropriate monitoring and measurement tools to capture and analyse these metrics.

**Documentation and Reporting:**
- Document the PoC setup, configuration, test results, and observations. Define the structure for your final PoC report, including sections for objectives, methodology, results, and conclusions.

