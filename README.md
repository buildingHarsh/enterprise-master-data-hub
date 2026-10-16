#Enterprise Master Data Hub with Data Quality Monitoring and Event-Driven Integration
This project is a simplified enterprise-grade Master Data Management (MDM) platform designed to improve the quality, reliability, and distribution of business data across multiple systems.
The platform accepts incoming master data (such as customers, products, suppliers, or employees) through MuleSoft APIs, validates the data using configurable quality rules, calculates quality scores, and stores trusted records in PostgreSQL. Every significant data change is published as an event through Apache Kafka, allowing downstream systems to consume updates independently and stay synchronized.
The solution also includes a SvelteKit dashboard that provides operational visibility into data quality metrics, system health, processing status, error rates, and Dead Letter Queue (DLQ) records.
Key Capabilities
Centralized master data ingestion through MuleSoft APIs
Data quality validation using DataWeave
Completeness checks
Validity checks
Consistency checks
Timeliness checks
Automated quality scoring and status classification
Persistent storage of master records and quality metrics in PostgreSQL
Event publication through Kafka for real-time data distribution
Dead Letter Queue (DLQ) handling for failed records
Error monitoring, retry mechanisms, and alerting
Hierarchical data processing (Customer → Orders → Order Items)
Real-time operational dashboard built with SvelteKit
End-to-end testing and monitoring
Business Problem Solved
Organizations often struggle with duplicate, incomplete, inconsistent, or outdated data spread across multiple applications. This project establishes a trusted source of master data, measures data quality before records are accepted, and ensures that updates are distributed reliably to other systems using an event-driven architecture.
Tech Stack
MuleSoft - Integration and orchestration layer
DataWeave - Data transformation and quality scoring
PostgreSQL - Master data and metrics storage
Apache Kafka - Event streaming and system integration
SvelteKit - Monitoring and administration dashboard
Docker - Local infrastructure management
MUnit - Automated testing
