# Flight Delay Time Statistics Dashboard

This project is a Dash-based web application that visualizes flight delay statistics for various airlines based on user-selected years. The dashboard provides insights into different types of flight delays through interactive line plots.

## Dashboard Components

The dashboard includes the following visualizations:
- **Monthly Average Carrier Delay**: Displays the average carrier delay time (in minutes) by reporting airline for the selected year.
- **Monthly Average Weather Delay**: Shows the average weather-related delay time (in minutes) by reporting airline for the selected year.
- **Monthly Average National Air System (NAS) Delay**: Presents the average NAS delay time (in minutes) by reporting airline for the selected year.
- **Monthly Average Security Delay**: Illustrates the average security-related delay time (in minutes) by reporting airline for the selected year.
- **Monthly Average Late Aircraft Delay**: Visualizes the average late aircraft delay time (in minutes) by reporting airline for the selected year.

## Prerequisites

To run the application, you need to install the following Python packages:

```bash
pip install packaging
pip install pandas dash
pip install httpx==0.20 dash plotly
```

## Code Summary

The application is built using Python and the Dash framework. Below is a summary of the key components:

- **Data Loading**: The application reads airline data from a CSV file (`airline_data.csv`) into a Pandas DataFrame, handling specific columns with string data types for consistency.
- **Dash Application**: A Dash app is created with a layout that includes:
  - A centered title ("Flight Delay Time Statistics").
  - An input field for selecting the year.
  - Five interactive line plots arranged in three segments: two plots side-by-side for carrier and weather delays, two for NAS and security delays, and a centered plot for late aircraft delays.
- **Compute Function (`compute_info`)**: This function filters the airline data by the user-selected year and computes the monthly average delays for carrier, weather, NAS, security, and late aircraft categories, grouped by airline.
- **Callback Function (`get_graph`)**: This function updates the five line plots dynamically based on the user’s year input. It uses Plotly Express to generate line plots for each delay type, with months on the x-axis, delay times on the y-axis, and different colors for each airline.
- **App Execution**: The Dash app runs and renders the interactive dashboard in a web browser.

## How to Run

1. Ensure all required packages are installed (see Prerequisites).
2. Place the `airline_data.csv` file in the same directory as the script.
3. Run the Python script containing the Dash application.
4. Open a web browser and navigate to the local server address (typically `http://127.0.0.1:8050`) to interact with the dashboard.


###Author - Luthfi Shaj