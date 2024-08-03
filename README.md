# Formula 1 Lap Time and Pit Stop Analysis

This repository contains a Python script to analyze and visualize Formula 1 lap times and pit stops for two drivers from two different races in the 2024 season. The analysis includes fetching data from the Ergast API, processing and displaying average lap times and pit stop durations, and solving differential equations to model lap times and pit stops.

## Features

- Fetch lap times and pit stop data from the Ergast API for specific drivers.
- Calculate and display average lap times and pit stop durations.
- Solve differential equations to model lap times and pit stops.
- Visualize the results using matplotlib.

## Requirements

- Python 3.7 or higher
- Requests library
- Pandas library
- Numpy library
- Scipy library
- Matplotlib library

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/f1-lap-time-analysis.git
    cd f1-lap-time-analysis
    ```

2. Install the required Python packages:
    ```sh
    pip install requests pandas numpy scipy matplotlib
    ```

## Usage

1. Run the script:
    ```sh
    python f1_analysis.py
    ```

2. The script will fetch the data, process it, and display the results in the console and as graphs.

## Script Overview

The main script (`f1_analysis.py`) performs the following steps:

1. Fetches lap times and pit stop data for specified races and drivers from the Ergast API.
2. Processes the fetched data to extract relevant information.
3. Calculates average lap times and pit stop durations.
4. Solves differential equations to model lap times and pit stops.
5. Displays the results in the console and visualizes the data using matplotlib.

## Functions

- `fetch_data(url)`: Fetches data from the provided API URL.
- `extract_lap_times(race_results)`: Extracts lap times from race results.
- `extract_pit_stops(pitstops)`: Extracts pit stop data.
- `fetch_and_extract_data(race_number, driver)`: Fetches and extracts data for a specific race and driver.
- `convert_time_to_seconds(time)`: Converts time in 'mm:ss.sss' format to seconds.
- `lap_time_model(t, y, driver)`: Differential equation function to model lap times.
- `display_pit_stops_and_lap_times()`: Displays pit stop and lap times for each driver.
- `print_results()`: Prints average lap times and pit stop durations.
- `display_graphs()`: Displays graphs comparing lap times and pit stop durations, and plots the differential equation results.

## Example Output

```plaintext
Average Lap Times:
  driverId  average_lap_time
0  norris       85.123
1  piastri      86.456

Average Pit Stop Durations:
  driverId  average_pitstop_duration
0  norris       3.456
1  piastri      3.789
