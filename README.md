# Climate Data Analysis Project

This project is designed to analyze climate data stored in a SQLite database. The data includes precipitation and temperature observations from multiple weather stations in Hawaii, spanning over a period of time. Using Python, SQLAlchemy, and Pandas, this project extracts, processes, and visualizes key climate trends.

## Project Overview

The project performs the following tasks:
- Reflects and connects to the database `hawaii.sqlite`.
- Retrieves and analyzes precipitation data for the last 12 months from the most recent date in the dataset.
- Calculates summary statistics for the precipitation data.
- Determines the number of weather stations in the dataset.
- Identifies the most active weather stations and retrieves temperature statistics for the most active station.
- Visualizes temperature data as a histogram for the most active station over the past 12 months.

## Tools Used

- Python 3.x
- SQLite (via `hawaii.sqlite` database)
- SQLAlchemy for database connection and ORM
- Pandas for data manipulation
- Matplotlib for plotting and visualization

## File Structure

- `hawaii.sqlite`: SQLite database containing the weather data.
- `climate_starter.ipynb`: Jupyter notebook containing the entire data analysis process, broken down into individual code cells.

## Getting Started

### Prerequisites

To run this project, you'll need to have the following Python libraries installed:
- sqlalchemy
- pandas
- matplotlib
- numpy

### Database Structure

The SQLite database `hawaii.sqlite` contains two tables:
1. `measurement`: This table holds the weather observations (e.g., precipitation, temperature).
2. `station`: This table contains information about the weather stations that made the observations.

### How to Run

1. Clone or download this repository.
2. Open the `climate_starter.ipynb` file in Jupyter Notebook.
3. Run each cell in order to perform the data analysis.
4. The notebook will output visualizations, summary statistics, and other insights based on the data.

### Key Analysis Steps

#### 1. Database Connection
The project starts by establishing a connection to the SQLite database `hawaii.sqlite` and reflecting its tables using SQLAlchemy.

#### 2. Precipitation Analysis
- **Objective**: Retrieve and analyze precipitation data for the last 12 months from the most recent date in the dataset.
- **Output**: A time series plot showing daily precipitation levels over the past year.

#### 3. Station Analysis
- **Objective**: Determine the total number of weather stations and identify the most active stations in terms of observations.
- **Output**: A list of stations and their corresponding observation counts, sorted in descending order.

#### 4. Temperature Analysis
- **Objective**: Retrieve and analyze temperature data for the most active station over the last 12 months.
- **Output**: A histogram showing the frequency of temperature observations at the most active station.

## Results

- The precipitation analysis shows the distribution of daily precipitation over the last 12 months, identifying periods of high rainfall.
- The temperature analysis identifies the lowest, highest, and average temperatures recorded at the most active station, with a histogram showing the temperature distribution over the past year.

## Closing Session

At the end of the analysis, the database session is closed to release resources.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Data provided by UC Irvine's Data Analytics Bootcamp.
- Tools and techniques taught during the bootcamp were instrumental in completing this project.
