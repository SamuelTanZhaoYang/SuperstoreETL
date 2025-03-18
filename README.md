# Superstore Data Pipeline for Cloud Integration & Data Warehousing

**Created by**: Samuel Tanzy  
**LinkedIn**: [www.linkedin.com/in/samuel-tan-zhao-yang-5391001ba](https://www.linkedin.com/in/samuel-tan-zhao-yang-5391001ba)

## Description

This project is a comprehensive ETL pipeline designed to load data into Google Cloud MySQL from CSV files, extract the data, transform it into a standardized format for analysis, and load it into a cloud-based data warehouse. The final deliverable is a robust data warehouse that centralizes data for efficient reporting and analytics, ensuring it is ready for business intelligence and decision-making.

## Purpose

The primary goal of this project is to automate the data ingestion process with minimal manual intervention, improving efficiency. By consolidating data into a data warehouse, the solution enables real-time analytics and provides a reliable foundation for data-driven strategies.

## Tech Stack

- **Languages**: Python
- **Frameworks & Libraries**:
  - **Pandas**: For data manipulation and cleaning
  - **SQLAlchemy**: For database operations and ORM
  - **Pydantic**: For data validation
  - **jpype1 & jaydebeapi**: For JDBC connectivity to databases
  - **google-cloud-bigquery**: For interacting with Google BigQuery
- **Databases/Cloud Services**:
  - **Google Cloud SQL**
  - **Google BigQuery**
  - **Data Warehouse**: A centralized repository for integrated data storage and analysis

## Prerequisites & Setup

### 1. Java Development Kit (JDK)

- **Requirement**: JDK-23
- **Action**: Download the installer and place it in the project directory.

**Download Links**:
- [Windows (x64 Installer)](https://download.oracle.com/java/23/latest/jdk-23_windows-x64_bin.exe)
- [macOS (x64 DMG Installer)](https://download.oracle.com/java/23/latest/jdk-23_macos-x64_bin.dmg)
- [Linux (x64 RPM Package)](https://download.oracle.com/java/23/latest/jdk-23_linux-x64_bin.rpm)

### 2. MySQL Connector/J

- **Requirement**: MySQL-connector for JDBC connectivity
- **Action**: Download the connector from MySQL Connector/J and extract it. Place the MySQL-connector folder into the project directory.

**Download Link**:  
[MySQL Connector/J](https://dev.mysql.com/downloads/connector/j?utm_source=chatgpt.com)

### 3. Cloud SQL Proxy

Cloud SQL Proxy is an executable that establishes a secure connection to your Cloud SQL instance, allowing connections from any IP address. It encrypts traffic using TLS and supports authentication via Google Cloud IAM.

**Setup Instructions**:
1. **Download the Executable**:  
   For Windows, download `cloud-sql-proxy.exe` and place it in your project directory (e.g., `C:\Users\tanzh\Documents\Gamuda Capstone\SuperstoreETL`). Make sure to download the latest version.

   **Download Link**:  
   [Cloud SQL Proxy Releases](https://github.com/GoogleCloudPlatform/cloud-sql-proxy/releases)

2. **Run the Proxy**:  
   Open a terminal (or Visual Studio PowerShell) and execute the following:

       ./cloud-sql-proxy --address 0.0.0.0 --port 3306 <INSTANCE_CONNECTION_NAME>

   Alternatively, for IAM authentication:

       ./cloud-sql-proxy --auto-iam-authn <INSTANCE_CONNECTION_NAME>

   **Note**: Port 3306 is used for connecting to MySQL.

## Installation

Before running the code, install the required Python dependencies using the following pip command:

    pip install pandas google-cloud-bigquery google-cloud-exceptions pydantic sqlalchemy jpype1 jaydebeapi

## Running the Project

### 1. Setup Environment
- Ensure that **JDK-23** and the **MySQL connector** are correctly placed in your project directory.
- Start the **Cloud SQL Proxy** to establish a secure connection with your Cloud SQL instance.

### 2. Install Dependencies
- Run the pip command mentioned above to install the required dependencies.

### 3. Execute the Notebooks or Scripts
- For ETL operations, run the notebooks or corresponding Python scripts.
- Verify that data is correctly loaded from CSV to Google Cloud MySQL, transformed as needed, and finally loaded into the data warehouse.

### 4. Monitor & Troubleshoot
- Check logs for errors during data extraction, transformation, or loading.
- Use the provided debugging tips or reach out to me on LinkedIn (be sure to introduce yourself).

## Additional Resources

- **Cloud SQL Proxy Video Tutorial**:  
  [Connecting to Google Cloud SQL with the Cloud SQL Proxy](https://www.youtube.com/watch?v=25XIGXbw_GY)

- **Official Documentation**:
  - [Google Cloud SQL Proxy Documentation](https://cloud.google.com/sql/docs/mysql/connect-auth-proxy)
  - [MySQL Connector/J Documentation](https://dev.mysql.com/doc/connector-j/8.0/en/)
  - [Google Cloud BigQuery Documentation](https://cloud.google.com/bigquery/docs)
