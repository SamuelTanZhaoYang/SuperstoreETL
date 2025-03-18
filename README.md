# Superstore Data Pipeline for Cloud Integration & Data Warehousing

Created by : Samuel Tanzy

Linkdln : www.linkedin.com/in/samuel-tan-zhao-yang-5391001ba

Description:

This project is a comprehensive ETL pipeline that involves loading data into Google Cloud MySQL from csv, and extracting the data from Google Cloud MySQL, transforms it into a standardized format for analysis, and loads it into a cloud-based data warehouse. The final deliverable is a robust data warehouse that centralises data for efficient reporting and analytics, ensuring that the data is immediately ready for business intelligence and decision-making.

Purpose:

The project was created to automate the data ingestion process while minimalising manual intervention and thus improving efficiency. By consolidating data into a data warehouse, the solution supports real-time analytics and provides a reliable foundation for data-driven strategies

Tech Stack:

Languages: Python

Frameworks & Libraries:

Pandas: For data manipulation and cleaning
SQLAlchemy: For database operations and ORM
Pydantic: For data validation
jpype1 & jaydebeapi: For JDBC connectivity to databases
google-cloud-bigquery: For interacting with Google BigQuery

Databases/Cloud Services:

Google Cloud SQL
Google BigQuery
Data Warehouse: A centralized repository for integrated data storage and analysis

Prerequisites & Setup:

1.  Java Development Kit (JDK)

Requirement: JDK-23
Action: Download the installer and place it in the project directory.

Download Links:

Windows (x64 Installer): https://download.oracle.com/java/23/latest/jdk-23_windows-x64_bin.exe

macOS (x64 DMG Installer):https://download.oracle.com/java/23/latest/jdk-23_macos-x64_bin.dmg

Linux (x64 RPM Package): https://download.oracle.com/java/23/latest/jdk-23_linux-x64_bin.rpm

2.  MySQL Connector/J

Requirement: MySQL-connector for JDBC connectivity
   
Action: Download the connector from MySQL Connector/J
   
Choose the platform independent version (download zip or tar for macOS), extract it, and paste the MySQL-connector folder into the project directory.

Download Link:

https://dev.mysql.com/downloads/connector/j?utm_source=chatgpt.com

3.  Cloud SQL Proxy

What It Is:

Cloud SQL Proxy is a separate executable that establishes a secure connection to your Cloud SQL instance, thus allowing one to connect in any IP address. Besides, it          encrypts traffic using TLS and supports authentication via Google Cloud IAM.

Setup Instructions:

1. Download the Executable:

For Windows, download the cloud-sql-proxy.exe and place it into your project directory (e.g., C:\Users\tanzh\Documents\Gamuda Capstone\SuperstoreETL). Note: Be sure to        check for the latest version of the executable

Download Link:

https://github.com/GoogleCloudPlatform/cloud-sql-proxy/releases

2. Run the Proxy:

Open a terminal (or Visual Studio PowerShell) and execute:

                ./cloud-sql-proxy --address 0.0.0.0 --port 3306 <INSTANCE_CONNECTION_NAME>

Alternatively, for IAM authentication:

                ./cloud-sql-proxy --auto-iam-authn <INSTANCE_CONNECTION_NAME>

Note: Port 3306 is used for connecting to MySQL.

Installation:

Before running the code, install the required Python dependencies. Use the following pip command:

                pip install pandas google-cloud-bigquery google-cloud-exceptions pydantic sqlalchemy jpype1 jaydebeapi

Running the Project

1. Setup Environment:

   Make sure that JDK-23 and the MySQL connector are correctly placed in your project directory.

   Start the Cloud SQL Proxy to establish a secure connection with your Cloud SQL instance.

2. Install Dependencies:
   
   Run the pip command mentioned above.

4. Execute the Notebooks or Scripts:

   For ETL operations, run the notebooks or corresponding Python scripts.

   Verify that the data is correctly loaded from CSV to Google Cloud MySQL, transformed as needed, and finally loaded into the data warehouse.

5. Monitor & Troubleshoot:

   Check logs for any errors during data extraction, transformation, or loading.

   Use debugging tips provided in the documentation if you encounter issues or contact me via LinkedIn (be sure to introduce yourself).

Additional Resources

Cloud SQL Proxy Video Tutorial:

 Connecting to Google Cloud SQL with the Cloud SQL Proxy
 Link: https://www.youtube.com/watch?v=25XIGXbw_GY

 Official Documentation:

 Google Cloud SQL Proxy Documentation
 Link: https://cloud.google.com/sql/docs/mysql/connect-auth-proxy

 MySQL Connector/J Documentation
 Link: https://dev.mysql.com/doc/connector-j/8.0/en/

 Google Cloud BigQuery Documentation
 Link: https://cloud.google.com/bigquery/docs
