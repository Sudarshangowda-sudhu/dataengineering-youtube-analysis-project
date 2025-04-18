# dataengineering-youtube-analysis-project
📊 YouTube Analysis Data Engineering Project
This project aims to securely manage, streamline, and analyze structured and semi-structured YouTube data based on video categories and trending metrics using AWS cloud services.


🔍 Overview
We process and analyze daily trending YouTube video data gathered from multiple countries. The pipeline performs ingestion, transformation, enrichment, and visualization using AWS services.

🎯 Project Goals
Data Ingestion: Fetch trending video data from multiple sources and store it in a centralized repository.

ETL System: Transform raw data into a structured format ready for analytics.

Data Lake: Store raw, cleansed, and enriched data centrally using Amazon S3.

Scalability: Use AWS cloud resources to handle growing data volumes efficiently.

Cloud-first: Leverage AWS for computation, storage, and analytics.

Reporting: Build interactive dashboards for insights and decision-making.

🛠️ AWS Services Used

Service	Description
Amazon S3	Scalable object storage used for raw, cleansed, and enriched data layers.
AWS IAM	Manages secure access to services and resources.
AWS Glue	Serverless data integration for ETL jobs and metadata cataloging.
AWS Lambda	Runs transformation scripts serverlessly.
AWS Athena	Interactive SQL querying directly on S3 data.
Amazon QuickSight	BI tool for dashboards and data visualization.
AWS CloudWatch	Monitoring and alerts for system health and pipeline failures.
AWS Step Functions	Orchestration for managing ETL workflow stages.
Amazon Redshift (Optional)	Data warehouse for complex analytical queries.
Power BI / Notebooks (Optional)	Additional visualization and analysis tools.
🧱 Architecture
The architecture follows a modular and scalable pattern:

Source Systems → S3 (Landing Zone via S3 API)

Data Lake:

Landing Area (Raw)

Cleansed/Enriched

Analytics/Reporting Layer

ETL Jobs via AWS Glue and AWS Lambda

Metadata Cataloging using AWS Glue Data Catalog

Data Access via AWS Athena and optional Redshift

Dashboarding with Amazon QuickSight and/or Qlik/Power BI

Monitoring using CloudWatch

Workflow Orchestration with AWS Step Functions

🧾 Dataset Used
Source: Trending YouTube Video Statistics - Kaggle

Format: CSV & JSON

Details:

Daily popular video stats across multiple countries

Fields: video title, channel, publication time, tags, views, likes, dislikes, comments, etc.

Contains category_id that maps to video categories from a separate JSON file

📈 Insights Enabled
Trending videos by region and time

Most popular categories

Engagement metrics (likes, dislikes, comments)

Channel-wise performance

Content trends across countries

🚀 How to Run
Upload data to the S3 Landing Area

Trigger ETL pipeline using AWS Step Functions

Transformed data moves through:

Cleansing (AWS Glue)

Enrichment (AWS Lambda / Glue)

Use Athena or Redshift to query data

Visualize with QuickSight, Qlik, or Power BI
