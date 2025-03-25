# Rain-Alert-SMS

This script retrieves weather forecast data from the OpenWeatherMap API and sends an SMS notification using the Twilio API if rain is predicted within the next 12 hours.

## Getting Started

## Features
- **Real-time Weather Monitoring**: Checks hourly forecasts from OpenWeatherMap
- **Instant SMS Alerts**: Sends notifications via Twilio when rain is detected
- **Configurable Location**: Set your exact latitude/longitude
- **Secure**: Uses environment variables for API credentials

## How It Works
1. Script runs and fetches weather data for your location
2. Analyzes next 12 hours of forecast data
3. If rain/snow is detected (>700 condition code):
   - Sends SMS via Twilio
   - Message includes umbrella emoji reminder ☔️
     
### Prerequisites

* Python 3.8+
* `requests` library (install with `pip install requests`)
* `twilio` library (install with `pip install twilio`)
* OpenWeatherMap API key (sign up at [openweathermap.org](https://openweathermap.org/))
* Twilio account (sign up at [twilio.com](https://www.twilio.com/))

### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Afeez07/Rain-Alert-SMS
    ```

2.  Navigate to the project directory:

    ```bash
    cd Rain-Alert-SMS
    ```

3.  Set the following environment variables:

    * `OWN_API_KEY`: Your OpenWeatherMap API key.
    * `AUTH_TOKEN`: Your Twilio auth token.
    * `https_proxy` : if you are using a proxy.

4.  Update the following variables in the Python script:

    * `account_sid`: Your Twilio account SID.
    * `YOUR LATITUDE`: Your latitude.
    * `YOUR LONGITUDE`: Your longitude.
    * `YOUR TWILIO VIRTUAL NUMBER`: Your Twilio virtual phone number.
    * `YOUR TWILIO VERIFIED REAL NUMBER`: Your real phone number (verified with Twilio).

5.  Run the script:

    ```bash
    python main.py
    ```

### Usage

The script will run once, get the weather data, and send an SMS if rain is predicted. To run it periodically, you can use a task scheduler (e.g., cron on Linux, Task Scheduler on Windows).

### Contributing

Feel free to contribute to RainAlertSMS by:

* Adding support for other weather conditions.
* Implement a more detailed weather forecast in the SMS.
* Adding support for other notification methods (e.g., email).
* Adding a GUI.
