# Real-Time-Data-Processing-System-for-Weather-Monitoring
### Objective
Build a real-time data processing system to monitor weather conditions and generate summarized insights using rollups and aggregates. The system will utilize data from the OpenWeatherMap API (https://openweathermap.org/).

### Data Source
The system will continuously fetch weather data from the OpenWeatherMap API. You'll need to sign up for a free API key to access the data. The API provides various weather parameters, and for this project, we will focus on:

- **main**: Main weather condition (e.g., Rain, Snow, Clear)
- **temp**: Current temperature in Celsius
- **feels_like**: Perceived temperature in Celsius
- **dt**: Time of the data update (Unix timestamp)

### Processing and Analysis
The system should continuously call the OpenWeatherMap API at a configurable interval (e.g., every 5 minutes) to retrieve real-time weather data for key cities in India: Delhi, Mumbai, Chennai, Bangalore, Kolkata, and Hyderabad.

For each weather update:
- Convert temperature values from Kelvin to Celsius (or Fahrenheit based on user preference).
- Continuously process and store weather data, while generating daily summaries. Alerts will be triggered when configured thresholds are crossed.

### Rollups and Aggregates

#### 1. Daily Weather Summary
- Aggregate weather data for each day.
- Calculate daily statistics:
  - **Average temperature**
  - **Maximum temperature**
  - **Minimum temperature**
  - **Dominant weather condition** (determined by the most frequent condition throughout the day)
- Store these daily summaries in a database or persistent storage for later analysis.

#### 2. Alerting Thresholds
- Allow users to set thresholds for temperature or specific weather conditions (e.g., trigger an alert if the temperature exceeds 35°C for two consecutive updates).
- Continuously monitor the latest weather data and compare it against these thresholds.
- Trigger alerts when thresholds are breached. Alerts can be displayed on the console or sent via email (implementation left open-ended).

#### 3. Implement Visualizations
- Create visualizations to display daily weather summaries, historical trends, and triggered alerts.

### Test Cases

#### 1. System Setup
- Ensure the system starts correctly and connects to the OpenWeatherMap API using a valid API key.

#### 2. Data Retrieval
- Simulate API calls at configurable intervals.
- Verify the system retrieves weather data for the specified locations and correctly parses the response.

#### 3. Temperature Conversion
- Test the conversion of temperature values from Kelvin to Celsius (or Fahrenheit) based on user preference.

#### 4. Daily Weather Summary
- Simulate weather updates over multiple days.
- Verify that daily summaries (average, max, min temperatures, and dominant weather condition) are calculated accurately.

#### 5. Alerting Thresholds
- Define and configure user-specific thresholds for temperature or weather conditions.
- Simulate weather data exceeding or crossing these thresholds.
- Confirm that alerts are only triggered when thresholds are breached.

### Getting Started

#### Prerequisites
- **ReactJs**
- **OpenWeatherMap API key**

#### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/username/weather-monitoring-system.git
    cd weather-wen-app/frontend
    ```

2. Install dependencies:
    ```bash
    npm i
    ```

3. Run the script:
    ```bash
    npm start
    ```

### Viewing Visualizations
- The application will display daily weather summaries, historical weather trends, and any triggered alerts on the web interface.
