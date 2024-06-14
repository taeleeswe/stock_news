# Stock Price Alert and News Notification System

This project is a Python script that monitors stock prices for a specific company and sends news alerts via SMS when significant changes are detected. The script uses the Alpha Vantage API for stock price data, the News API for news articles, and Twilio for sending SMS messages.

## Prerequisites

To run this script, you'll need the following:

1. **Python 3.x** installed on your machine.
2. **API keys** for Alpha Vantage and News API.
3. **Twilio account** with account SID, auth token, and a registered Twilio phone number.

## Environment Variables

Before running the script, set the following environment variables:

- `STOCK_API_KEY` : Your Alpha Vantage API key.
- `NEWS_API_KEY` : Your News API key.
- `TWILIO_AID` : Your Twilio Account SID.
- `TWILIO_TOKEN` : Your Twilio Auth Token.
- `TWILO_NUM` : Your Twilio phone number (the sender).
- `OWN_PHONE_NUM` : Your personal phone number (the receiver).

## How it Works
1. **Stock Price Monitoring**: The script fetches the daily stock prices for a specified company from Alpha Vantage.
2. **Percentage Change Calculation**: It calculates the percentage change in the stock price between yesterday and the day before yesterday.
3. **News Fetching**: If the stock price change exceeds a specified threshold (5% by default), the script fetches the latest news articles about the specified company from the News API.
4. **SMS Notification**: The script formats these news articles and sends them via SMS to the specified phone number using Twilio.



**You can set these environment variables in your shell or create a `.env` file in your project directory with the following content:**

```plaintext
STOCK_API_KEY=your_alpha_vantage_api_key
NEWS_API_KEY=your_news_api_key
TWILIO_AID=your_twilio_account_sid
TWILIO_TOKEN=your_twilio_auth_token
TWILO_NUM=your_twilio_phone_number      
OWN_PHONE_NUM=your_phone_number



