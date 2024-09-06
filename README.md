# Climate Data Analysis Project

This project is designed to analyze climate data stored in a SQLite database. The data includes precipitation and temperature observations from multiple weather stations in Hawaii, spanning over a period of time. Using Python, SQLAlchemy, Pandas, and Flask, this project extracts, processes, and visualizes key climate trends while providing a RESTful API for easy data access.

## Project Overview

The project performs the following tasks:
- Reflects and connects to the database `hawaii.sqlite`.
- Retrieves and analyzes precipitation data for the last 12 months from the most recent date in the dataset.
- Calculates summary statistics for the precipitation data.
- Determines the number of weather stations in the dataset.
- Identifies the most active weather stations and retrieves temperature statistics for the most active station.
- Visualizes temperature data as a histogram for the most active station over the past 12 months.
- Provides a Flask-based REST API that delivers climate data via several endpoints.

## Tools Used

- Python 3.x
- SQLite (via `hawaii.sqlite` database)
- SQLAlchemy for database connection and ORM
- Pandas for data manipulation
- Matplotlib for plotting and visualization
- Flask for building the REST API

## File Structure

- `hawaii.sqlite`: SQLite database containing the weather data.
- `climate_starter.ipynb`: Jupyter notebook containing the data analysis process.
- `app.py`: Flask application that serves as a REST API for accessing the climate data.

## Getting Started

### Prerequisites

To run this project, you'll need to have the following Python libraries installed:
- sqlalchemy
- pandas
- matplotlib
- numpy
- flask

### Database Structure

The SQLite database `hawaii.sqlite` contains two tables:
1. `measurement`: This table holds the weather observations (e.g., precipitation, temperature).
2. `station`: This table contains information about the weather stations that made the observations.

### How to Run the Jupyter Notebook

1. Clone or download this repository.
2. Open the `climate_starter.ipynb` file in Jupyter Notebook.
3. Run each cell in order to perform the data analysis.
4. The notebook will output visualizations, summary statistics, and other insights based on the data.

### How to Run the Flask API

1. Ensure you have Flask installed.
2. Run the Flask application (`app.py`) from your terminal.
3. The application will be hosted locally, and you can access the following API routes via your browser or a tool like Postman.

## Flask API Routes

The Flask app provides several endpoints for accessing the climate data:

- `/api/v1.0/precipitation`: Returns the precipitation data for the last year as a JSON dictionary.
- `/api/v1.0/stations`: Returns a JSON list of all weather stations from the dataset.
- `/api/v1.0/tobs`: Returns temperature observations for the most active station for the last year as a JSON list.
- `/api/v1.0/<start>`: Returns the minimum, average, and maximum temperatures for all dates greater than or equal to the specified start date.
- `/api/v1.0/<start>/<end>`: Returns the minimum, average, and maximum temperatures for the date range specified between start and end.

### Key Analysis Steps in Jupyter Notebook

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

## Acknowledgments

- Data provided by UC Irvine's Data Analytics Bootcamp.
- Tools and techniques taught during the bootcamp were instrumental in completing this project.

