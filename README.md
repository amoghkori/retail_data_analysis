# Retail Data Analysis (End-to-End)

This project is an end-to-end retail data analysis pipeline, designed to provide real-time insights into retail operations. It leverages a combination of cloud services, programming languages, and data visualization tools to transform raw data into actionable intelligence.

## Project Overview

The pipeline begins by ingesting raw retail data into AWS S3, which then gets transformed and loaded into Snowflake for advanced querying and analysis. The data transformation and table setup processes are handled using Python and SQL within a Jupyter Notebook environment. For the final step, an interactive Tableau dashboard provides real-time insights by connecting to Snowflake, ensuring that the data is always up-to-date thanks to a combination of Snowpipe and a scheduled CRON job in Jupyter Lab, which is connected to Amazon SQS for event-driven data processing.

## Technologies Used

- **AWS S3**: Used for storing raw data.
- **Snowflake**: Serves as our data warehousing solution, allowing for scalable and efficient data analysis.
- **Python**: Used for data transformation and interaction with AWS services.
- **SQL**: Utilized within Snowflake to query and manipulate data.
- **Jupyter Notebook**: The environment where Python scripts are executed.
- **Tableau**: For creating interactive dashboards that provide insights into the data.
- **Snowpipe**: Facilitates continuous data ingestion into Snowflake.
- **Amazon SQS**: Manages message queues for communication between different services.
- **CRON Job**: Scheduled within Jupyter Lab to regularly trigger data refreshes in Tableau.

## Architecture

1. Data is ingested from various sources into **AWS S3**.
2. **Snowpipe** integrates with AWS to ensure data is continuously updated.
3. **Python** scripts within a **Jupyter Notebook** transform the data and load it into **Snowflake**.
4. **SQL** is used within Snowflake to further refine the data and prepare it for analysis.
5. An **interactive Tableau dashboard** connects to Snowflake to visualize the data.
6. A **CRON job** in Jupyter Lab, connected to **Amazon SQS**, triggers regular data refreshes in the Tableau dashboard.




