# NYC_Yellow_Taxi_Data_Pipeline-2024-

This script performs ETL (Extract, Transform, Load) operations on the New York City Yellow Taxi data for the year 2024. It reads monthly .parquet files, cleans the data, and uploads it to a PostgreSQL database for further analysis.

📁Project Structure
nyc_yellow_taxi_etl/
* yellow_taxi_etl.py      # Main ETL script
* README.md               # This documentation file
* yellow_tripdata_2024-*.parquet  # Monthly source data files (Jan to Dec)

🚀** What the Code Does**
1. Extract
Reads monthly NYC Yellow Taxi trip data from .parquet files.
Files are named in the format: yellow_tripdata_2024-01.parquet to yellow_tripdata_2024-12.parquet.

2. Transform
Checks for and removes rows with missing values (NaN).
Converts the passenger_count column from float to int for data consistency.

3. Load
Establishes a connection to a PostgreSQL database.
Loads the cleaned dataset into a table named nyc_yello_taxi.

🧪 Requirements
pip install pandas numpy sqlalchemy psycopg2 pyarrow

⚙️ Configuration
* PostgreSQL running locally on port 5432.
* A database named
* A user: postgres with password

✅ Output

A table named nyc_yello_taxi in your PostgreSQL database containing the cleaned data from all 12 months.


<img width="464" alt="image" src="https://github.com/user-attachments/assets/e9c2ce7a-055d-443a-aec8-7f8ab0d5d922" />
