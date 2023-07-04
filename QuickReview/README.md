# Quick review <!-- omit in toc -->

## Table of contents <!-- omit in toc -->

- [Service tiers](#service-tiers)
  - [Develop Azure Compute Solutions](#develop-azure-compute-solutions)
    - [Infrastructure as a Service](#infrastructure-as-a-service)
    - [Azure App Service](#azure-app-service)
    - [Azure Functions](#azure-functions)
  - [Develop for Azure Storage](#develop-for-azure-storage)
    - [Azure Cosmos DB](#azure-cosmos-db)
    - [Azure Blob Storage](#azure-blob-storage)
  - [Implement Azure Security](#implement-azure-security)
    - [Azure Key Vault](#azure-key-vault)
  - [Monitor, Troubleshoot \& Optimize Azure Solutions](#monitor-troubleshoot--optimize-azure-solutions)
    - [Azure Cache for Redis](#azure-cache-for-redis)
    - [Azure Content Delivery Networks](#azure-content-delivery-networks)
  - [Connect To and Consume Azure Services and Third-Party Services](#connect-to-and-consume-azure-services-and-third-party-services)
    - [API Management](#api-management)
    - [Event Hubs](#event-hubs)
    - [Azure Service Bus](#azure-service-bus)

## [Service tiers](https://azure.microsoft.com/en-us/pricing/#product-pricing)

### Develop Azure Compute Solutions
#### Infrastructure as a Service

- Azure Container Registry
  ||Basic|Standard|Premium|
  |---|---|---|---|
  **Included storage**| 10 GB|100 GB|500 GB
  **Total web hooks**|2|10|100|
  |**Geo Replication**|-|-|X
  |**Enhanced throughput for docker pulls**|-|-|X

- Azure Container Instances
  - **Pay as you go**
  - **Savings plan (1/3 years)**
  
- Azure Container Apps
  - **Consumption plan**
  - **Dedicated plan**

#### Azure App Service

||Free|Shared|Basic|Standard|Premium|Isolated|
|---|---|---|---|---|---|---|
|**Apps**|10|100|Unlimited|Unlimited|Unlimited|Unlimited|
|**Disk space**|1 GB|1 GB|10 GB|50 GB|250 GB|1 TB
|**Maximum instances**|- |-|Up to 3|Up to 10|Up to 30|Up to 100
|**Custom domain**|-|X|X|X|X|X
|**Auto scale**|-|-|-|X|X|X|X|
|**Deployment slots**|-|-|-|X|X|X|
**Hybrid connectivity**|-|-|X|X|X|X|
|**VNet connectivity**|-|-|X|X|X|X|
|**Private endpoints**|-|-|X|X|X|X|
|**Compute type**|Shared|Shared|Dedicated|Dedicated|Dedicated|Isolated

#### Azure Functions

- **Consumption plan**
- **Premium plan**
  - Pre-warmed workers
- **Dedicated plan**
  - App service plan

### Develop for Azure Storage
#### Azure Cosmos DB

Account modes

- **Provisioned thoughput**
  - Provision number of RUs per second
  - Scaling by increasing/decreasing RUs
- **Serverless**
  - No provisioning
  - Billed at the end of billing period for consumed RUs

#### Azure Blob Storage

- **Standard (GPv2)**
  - Access tiers
- **Premium**
  - No access tiers
  - Block & append blobs with low & consistent latency
### Implement Azure Security
#### Azure Key Vault

- **Standard**
- **Premium**
  - HSM encryption

### Monitor, Troubleshoot & Optimize Azure Solutions
#### Azure Cache for Redis

||Basic|Standard|Premium|Enterprise|Enterprise Flash|
|---|---|---|---|---|---|
|**Memory size**|250 MB - 53 GB|250 MB - 53 GB|6 GB - 120 GB| 12 GB - 100 GB| 384 GB - 1.5 TB|
|**SLA**|-|Up to 99.9%|Up to 99.9%|Up to 99.999%|Up to 99.999%|
|**Azure Private Link**|X|X|X|X|X
|**Replication & failover**|-|X|X|X|X
|**Zone redundancy**|-|-|X|X|X|
|**Redis data persistence**|-|-|X|X|X|
|**Redis cluster**|-|-|X|X|X|
|**Vitual network**|-|-|X|-|-
|**Geo replication**|-|-|Passive|Active|Active
|**RedisSearch**|-|-|-|X|X
|**RedisJSON**|-|-|-|X|X|
**RedisBloom**|-|-|-|X|-
|**RedisTimeSeries**|-|-|-|X|-|
|**Redis on Flash (non-volatile memory)**|-|-|-|-|X
|**Max number of client connections**|256 - 20.000|256 - 20.000|7.500 - 40.000|50.000 - 200.000|50.000 - 120.000|


#### [Azure Content Delivery Networks](https://learn.microsoft.com/en-us/azure/cdn/cdn-features)


| |Standard from Microsoft|Standard from Akamai|Standard from Verizon|Premium from Verizon|
|---|---|---|---|---|
|**Adaptive image compression**|-|X |-|-|
|**Object prefetching**|-|X|-|-|
|**Change optimization type**|-|X|-|-
|**Asset preloading**|-|-|X|X|
|**Token authentication**|-|-|-|X|
|**Cache/header settings**|X|Only using caching rules|Only using caching rules|X
|**URL redirect/rewrite**|X|-|-|X|
|**Customizable rules-based CD engine**|X|-|-|X|

### Connect To and Consume Azure Services and Third-Party Services
#### API Management

| |Consumption|Developer |Basic|Standard|Premium |Isolated|
|---|---|---|---|---|---|---|
|**Developer portal**|-|X|X|X|X|X|
|**Internal cache**|-|X|X|X|X|X|
|**Internal cache size**|-|10 MB|50 MB|1 GB|5 GB|5 GB|
|**External cache**|X|X|X|X|X|X|
|**Scaling units**|Automatic|1|2|4|12 per region|12 per region|
**SLA**|99.95%|-|99.95%|99.95%|99.99%|99.99%|
|**Isolation**|Shared|Private|Private|Private|Private|Private

#### Event Hubs

||Basic|Standard|Premium|Dedicated|
|---|---|---|---|---|
|**Capacity**|Throughput units|Throughput units|Processing units (PU)|Capacity units (CU)
|**Capture**|-|X|X|X|
|**Apache Kafka**|-|X|X|X|
|**Schema Registry**|-|X|X|X|
|**Max retention period**|1 day|7 days|90 days|90 days
|**Storage retention**|84 GB|84 GB|1 TB per PU|10 TB per CU

#### Azure Service Bus
||Basic|Standard|Premium|
|---|---|---|---|
|**Message size**|256 KB|256 KB|100 MB|
|**Queues**|X|X|X|
|**Scheduled messages**|X|X|X|
|**Topics**|-|X|X|
|**Transactions**|-|X|X|
|**De-duplication**|-|X|X|
|**Sessions**|-|X|X|
|**ForwardTo/SendVia**|-|X|X|
|**Resource isolation**|-|-|X|
|**Geo-Disaster recovery**|-|-|X|
|**Java Messaging Service support**|-|-|X|
|**Availability Zones support**|-|-|X|
