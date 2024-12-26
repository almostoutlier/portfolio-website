---
title: 2021 Olympic Analysis
slug: case-study-2
date: '2024-12-25'
excerpt: ''
featuredImage:
  url: /images/900px-Olympic_flag.svg_.png
  altText: Case study 2
  styles:
    self:
      borderRadius: x-large
  type: ImageBlock
bottomSections:
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
isFeatured: true
colors: bg-light-fg-dark
styles:
  self:
    padding:
      - pt-5
      - pl-5
      - pb-5
      - pr-5
    textAlign: center
    borderColor: border-light
    borderStyle: none
    borderWidth: 0
    borderRadius: none
    flexDirection: col
type: PostLayout
---
## Project Overview



This comprehensive data engineering project focuses on the Tokyo Olympics 2021 dataset, demonstrating an end-to-end data pipeline using various Azure services. The project aims to process, analyze, and visualize data from over 11,000 athletes participating in 47 disciplines across 743 teams.

## About the Dataset



Our dataset provides a rich tapestry of information about the Tokyo Olympics 2021, including:

*   Detailed profiles of over 11,000 athletes

*   Information on 47 distinct sporting disciplines

*   Data on 743 participating teams

*   Comprehensive entries categorized by gender

*   Athletes' names, countries represented, and disciplines

*   Gender distribution of competitors

*   Names and details of coaches

This diverse dataset allows for multifaceted analysis of Olympic participation, performance, and representation.

## Tech Stack



We leverage a robust suite of Azure services to build our data pipeline:

1.  **Azure Data Factory**: For efficient data ingestion and orchestration

2.  **Azure Data Lake Gen 2**: Serving as our primary data repository

3.  **Azure Blob Storage**: For cost-effective storage of raw and processed data

4.  **Azure Databricks**: Powering our data transformation processes

5.  **Azure Synapse Analytics**: Enabling advanced data analytics and SQL querying

6.  **Power BI**: For creating interactive dashboards and visual reports

## Project Pipeline

![](https://github.com/almostoutlier/Projects/blob/main/Olympics/images/flow.png?raw=true)





Our data engineering pipeline consists of the following key stages:

1.  **Data Ingestion**: Raw data acquisition from GitHub repository

2.  **Data Storage**: Storing raw data in Azure Blob Storage

3.  **Data Transformation**: Processing and cleaning data using Azure Databricks

4.  **Processed Data Storage**: Storing transformed data in Azure Data Lake Gen 2

5.  **Data Analytics**: Performing in-depth analysis using Azure Synapse Analytics

6.  **Data Visualization**: Creating insightful dashboards with Power BI

## Setup Instructions



1.  **Azure Account Setup**:

    *   Obtain an Azure account using the GitHub Student Pack for free credits

    *   Create a new Resource Group for this project

2.  **Data Source Preparation**:

    *   Ensure the GitHub repository containing the raw Olympics data is accessible

3.  **Azure Services Configuration**:

    *   Create an Azure Storage account for resource management

    *   Set up Azure Data Factory for data ingestion

    *   Configure Azure Databricks workspace

    *   Establish Azure Synapse Analytics workspace

4.  **Access Management**:

    *   In the Azure Portal, navigate to the IAM (Identity and Access Management) console

    *   Grant read and write permissions to the Azure Blob Storage Container for Databricks access

5.  **Authentication**:

    *   Azure Databricks uses Single Sign-On (SSO) with Azure, simplifying authentication

### Resources



This project uses several Azure resources:

*   **Azure Data Factory (olympic-df)**

*   **Azure Databricks (olympic-df-vir)**

*   **Storage Account (olympicdatasavir)**

![](https://github.com/almostoutlier/Projects/raw/main/Olympics/images/resources.png)



## Data Ingestion



The data ingestion process is implemented using Azure Data Factory, a cloud-based ETL and data integration service. Here's an overview of the steps:

1.  **Source Configuration**:

    *   Created a new pipeline in Azure Data Factory

    *   Configured an HTTP connector to connect to the GitHub repository containing the raw Olympic data

2.  **Sink Configuration**:

    *   Established a connection to Azure Blob Storage as the destination for raw data

    *   Created a dataset representing the target location in Blob Storage

3.  **Copy Activity Setup**:

    *   Implemented a Copy Activity within the Azure Data Factory pipeline

    *   Configured the source (HTTP) and sink (Blob Storage) connections

    *   Set up appropriate column mappings to ensure data is correctly transferred

4.  **Pipeline Execution**:

    *   Executed the pipeline to transfer data from GitHub to Azure Blob Storage

    *   Monitored the pipeline run for successful completion and any potential errors

5.  **Scheduling and Monitoring**:

    *   Set up a trigger to run the pipeline on a regular schedule (e.g., daily updates if new data is available)

    *   Implemented monitoring and alerting to track the health and performance of the ingestion process

This ingestion process ensures that our raw Olympic data is reliably transferred from the source GitHub repository to Azure Blob Storage, setting the stage for subsequent transformation and analysis steps in our data pipeline.

![](https://github.com/almostoutlier/Projects/raw/main/Olympics/images/pipeline.png)



## Data Storage



After transformation, the processed data is stored in Azure Data Lake Gen 2, providing a scalable and secure solution for big data analytics.

## Data Cleaning & Analytics



*   **Link to Databricks Publication:** [Olympic Analysis Using Spark](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/2985497818835596/194652377457841/8099496849479748/latest.html)

## Installation



1.  Clone the repository:

2.  Navigate to the project directory:

3.  Install the required libraries:

## Usage



1.  Set up the Azure resources as shown in the resources section.

2.  Open the Jupyter Notebook:

3.  Follow the instructions in the notebook to run the data analysis and visualization.

## Future Enhancements



*   Implement real-time data ingestion for live Olympic events

*   Develop predictive models for athlete performance using Azure Machine Learning

*   Expand the dataset to include historical Olympic data for trend analysis

## Conclusion



This project demonstrates the power of Azure's data services in handling large-scale sports analytics. By leveraging this robust ecosystem, we've transformed raw Olympic data into actionable insights, providing a comprehensive view of the Tokyo Olympics 2021.



