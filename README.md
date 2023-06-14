# Analysis of Songs Data

This project was designed to analyze what kind of songs different users are listening to or the so called **'Song Play Analysis'** for a startup called **Sparkify**. The main goal is compare the results of the analysis team with the results in this project. It involves building an ETL pipeline that extracts data from an S3 bucket where the song and log data resides in AWS, then processes them in Spark, transforms the data into a set of dimensional tables and loads the data back into an S3 bucket.

## Getting Started

### Prerequisites

- **Python3**

Install python3 using the below code for Windows or Mac OS.

> {'sudo apt-get install python', 'brew install python'}

- **Code editor like VS Code or Jupiter Notebook**

    - Jupiter notebook can be installed using Anaconda or pip
    
> {'sudo apt-get install code', 'python -m pip install --upgrade pip'} 

- **Amazon Web Services Account**

    - A valid AWS account is required in order to host the EMR cluster in AWS
    - Refer the link 'https://portal.aws.amazon.com/billing/signup'
    
- **Knowledge of Cluster creation, IAM, EC2, User creation**

    - Refer the link 'https://aws.amazon.com/solutions/implementations/data-lake-solution/'

### Running Python Scripts

The code below can be used to run the python scripts in the terminal for Python version 3 and above.

> python3 file_name.py

## Roadmap

1. etl.py

Performs the staging process where data is loaded from the S3 bucket into the DB and finally to the dimensinal tables. Processes individual song and log data into tables.

2. dl.cfg

Contains the EMR cluster details that is used by etl.py

## Database Schema 

Star schema was used to implement the database due its simplicity and less execution time for queries. Although it has high data redundancy the interdependency between tables is reduced, thereby reducing the query complexity.

## ETL Pipeline

The **pyspark** module from Python was used to extract, transform and load the data to SQL as it has high code readabilty and performance. The final data into the dimensinal tables is loaded by the staging process that contains the ETL pipeline.

## License

This project is licensed under Sparkify License



