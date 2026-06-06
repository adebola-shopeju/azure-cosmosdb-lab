# Azure Cosmos DB Setup — Lab Assignment

## Project Summary
This project configures and deploys an Azure Cosmos DB account using the NoSQL (Core SQL) API. It demonstrates global distribution, container partitioning, CRUD operations, throughput management, security controls, and monitoring.

## Configuration Choices

### API: Core SQL (NoSQL)
The Core SQL API was selected because it supports rich SQL-like queries against JSON documents, is the most feature-complete Cosmos DB API, and is the recommended starting point for new workloads.

### Consistency Level: Session
Session consistency was selected because it guarantees that a user always reads their own writes within a session the right balance for most application workloads. Strong consistency was not chosen because it limits throughput and increases latency.

### Partition Key: /category
The /category field was chosen as the partition key because it has multiple distinct values (electronics, clothing, books), distributes data evenly across partitions, and is a common query filter.

## Screenshots
See the screenshots uploaded in this repository.

## Notes on Setup
During setup, the following adjustments were made from the original guide:
- A second resource group (rg-cosmolab2) was created because the first was restricted to EUAP preview regions
- East US was selected as the primary region instead of South Africa North due to availability constraints
- West US 2 was added as the read replica region
