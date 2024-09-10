# Data Modelling with Apache Cassandra
[![GitHub](https://badgen.net/badge/icon/GitHub?icon=github&color=black&label)](https://github.com/MaxineXiong)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with Python](https://img.shields.io/badge/Python->=3.6-blue?logo=python&logoColor=white)](https://www.python.org)

<br>

## Project Description

This project focuses on building an Apache Cassandra database for *Sparkify*, a startup that offers music streaming services. Sparkify collects large amounts of user activity and song data, and the analytics team wants to query this data to better understand user behaviour, specifically around song preferences. The goal is to create an ETL pipeline to preprocess raw event data stored in multiple CSV files, consolidate it, and design a Cassandra data model to support queries on the song play data.

<br>

## Project Data

The dataset contains user activity data from *Sparkify*'s app, partitioned by date in the `event_data` folder. Each CSV file represents a day's worth of events. For instance:

```
event_data/2018-11-08-events.csv
event_data/2018-11-09-events.csv
```

These files include information on song titles, user details, and session data, as the image below shows.


<br>

## Repository Structure

The repository is organized as follows:

```
Data_Modelling_with_Apache_Cassandra/
├── Project_Data_Modelling_with_Apache_Cassandra.ipynb
├── event_data/
├── .gitignore
├── README.md
└── LICENSE
```

- **Project_Data_Modelling_with_Apache_Cassandra.ipynb**: Jupyter notebook containing the ETL pipeline code for pre-processing data and modelling it in Apache Cassandra.
- **event_data/**: Directory containing the original CSV files partitioned by date.
- **.gitignore**: Specifies files and directories that Git should ignore (e.g., system files, large data files).
- **README.md**: Provides an overview of the project.
- **LICENSE**: The license governing the usage of this project.

<br>

## Usage

1. **Pre-requisites**:
    - Python 3.7 or higher
    - Apache Cassandra installed and running
    - Jupyter Notebook (optional for running the `.ipynb` file)
2. **Steps**:
    - Run the Jupyter notebook `Project_Data_Modelling_with_Apache_Cassandra.ipynb`.
    - The notebook will pre-process the data by consolidating the partitioned files into a single streamlined CSV. It then will design and create tables in Apache Cassandra based on the queries provided by *Sparkify*, and finally, will insert data from the CSV into those tables using CQL commands.
    - You can modify the queries or data model to suit your needs.

<br>

## Contribution

Contributions to improve the project are welcome. Please open an issue or submit a pull request with your suggestions or bug fixes.

<br>

## **License**

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/). Feel free to use, modify, and distribute the application in accordance with the terms of the license.

<br>

## Acknowledgement

This project was completed as part of the Data Engineering Nanodegree at Udacity. Special thanks to [Udacity](https://www.udacity.com/) for providing the datasets and project specifications.
