# YouTube Trending Data Lake (AWS)

## Project Overview

This project builds a fully serverless data lake on AWS to analyze YouTube trending video data across multiple countries.

The system ingests raw CSV and JSON files, stores them in Amazon S3 using partitioned folders, automatically discovers schema using AWS Glue Crawlers, and enables SQL-based analytics using Amazon Athena.

The entire architecture runs without managing any servers.

---

## Architecture

Local Dataset  
→ Amazon S3 (Partitioned Data Lake)  
→ AWS Glue Crawler  
→ Glue Data Catalog  
→ Amazon Athena (SQL Analytics)

---

## AWS Services Used

- Amazon S3 (Data Lake Storage)
- AWS Glue Crawler (Schema Discovery)
- Glue Data Catalog (Metadata Management)
- Amazon Athena (Serverless SQL Queries)
- IAM (Access Control)

---

## Data Structure

Raw data is stored in S3 using partitioned folders:

youtube/raw_statistics/region=us/  
youtube/raw_statistics/region=gb/  
youtube/raw_statistics/region=ca/  
etc.

This improves query performance and enables scalable analytics.

---

## Example Queries

- Count total records
- Count rows per region
- Total views by region
- Average views by region
- Top channels by total views

All queries are executed using Amazon Athena.

---

## Key Features

- Fully serverless architecture
- Partitioned data lake design
- Automated schema detection using Glue
- SQL analytics without provisioning infrastructure
- Scalable and cost-efficient

---

## Project Status

Completed and fully functional.

---


## Sample Query Results


- Query Results  (screenshots/Query1.png,  screenshots/Query2.png,  screenshots/Query3.png)

- S3 Partition Structure (screenshots/S3-Structure1.png, screenshots/S3-Structure2.png)


---


## Key Highlights

- 400,000+ records processed
- 10-country partitioned dataset
- Serverless architecture (no infrastructure management)
- Cost-optimized using partitioned S3 layout
- SQL-based analytics via Amazon Athena

