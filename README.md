# Marketing Campaign Data Analysis using PySpark

This project analyzes marketing campaign data using PySpark, a fast and scalable data processing framework. It performs various analytical tasks such as counting events by campaign, date, hour, and event type, as well as analyzing events by store and user demographics. The project also includes storing the processed data in HDFS and creating external Hive tables for querying.

## Installation
To run this project, you need to have PySpark installed. You can install PySpark using pip:

```bash
pip install pyspark
```

## Usage
1. Clone the repository to your local machine.
2. Ensure you have access to a Hadoop Distributed File System (HDFS) and a Spark environment.
3. Place the provided JSON files (`ad_campaigns_data.json`, `user_profile_data.json`, `store_data.json`) in your HDFS.
4. Run the Jupyter notebook containing the PySpark code to perform the analysis.

## Data
The project uses three JSON files for data analysis:
- `ad_campaigns_data.json`: Contains data about marketing campaigns, including campaign ID, event type, and event time.
- `user_profile_data.json`: Contains user profile data, including user ID, demographics, and categories.
- `store_data.json`: Contains store data, including store names and associated place IDs.

## Querying Data with HQL
You can query the processed data using Hive Query Language (HQL) from the command-line interface (CLI) as follows:

1. Open your terminal or command prompt.
2. Use the `hive` command to start the Hive CLI.
3. Run HQL queries to analyze the data stored in the external Hive tables created by the project.

Example HQL query:

```sql
SELECT * FROM Output1;
```

## Analysis
The analysis includes the following tasks:

### Q1. Analyze data by campaign, date, hour, and operating system (os_type) to count events.
- Output path: `/Spark/Assignment1/Output1/`

### Q2. Analyze data by campaign, date, hour, and store name to count events.
- Output path: `/Spark/Assignment1/Output2/`

### Q3. Analyze data by campaign, date, hour, and gender to count events.
- Output path: `/Spark/Assignment1/Output3/`

## Results
The results of the analysis are stored in JSON format in the specified output paths. Each output directory contains analyzed data for the respective analytical task.

## Contributing
Contributions to this project are welcome. You can contribute by:
- Reporting bugs or issues
- Suggesting new features or enhancements
- Submitting pull requests

## License
This project is licensed under the [MIT License](LICENSE).
