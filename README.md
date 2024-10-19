# StocksLivePrice

**StocksLivePrice** is a web application that provides real-time stock prices and market data using the AlphaVantage API. The app uses SignalR to push live updates to the frontend, making it an ideal solution for monitoring stock prices dynamically. 

## Features
- Real-time stock price updates using SignalR.
- Dashboard to track multiple stock tickers.
- Dark mode support for a better user experience.
- Interactive stock charts powered by Chart.js.
- Integration with AlphaVantage API for reliable stock data.

## Tech Stack
- **Frontend:** HTML, Tailwind CSS, Chart.js, SignalR
- **Backend:** ASP.NET Core, SignalR, AlphaVantage API
- **Database:** PostgreSQL (Npgsql)
- **API:** AlphaVantage API
- **Hosting:** Self-hosted or cloud-based environments

## Prerequisites

- .NET 6.0 SDK or later
- PostgreSQL database
- AlphaVantage API Key (You can sign up [here](https://www.alphavantage.co/))

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/abdorhl/StocksLivePrice.git
   cd StocksLivePrice
   ```

2. **Install dependencies:**
   Make sure you have installed the required dependencies by restoring the .NET packages:
   ```bash
   dotnet restore
   ```

3. **Set up PostgreSQL Database:**
   Update the connection string in `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "Database": "Host=localhost;Port=5432;Database=stocksdb;Username=youruser;Password=yourpassword"
   }
   ```

4. **Set up AlphaVantage API Key:**
   In the `appsettings.json`, add your API key:
   ```json
   "Stocks": {
     "ApiUrl": "https://www.alphavantage.co",
     "ApiKey": "your_api_key"
   }
   ```

5. **Run the application:**
   ```bash
   dotnet run
   ```

6. **Access the application:**
   Open your browser and go to `https://localhost:5001`.

## Usage

- Enter a stock ticker symbol (e.g., AAPL, MSFT) in the input field to track its price in real-time.
- The application displays the current price, percentage change, and a small chart showing price trends.

## API Endpoints

- `GET /api/stocks/{ticker}`: Fetches the latest stock price for a given ticker.
  
## License

This project is licensed under the MIT License.

## Acknowledgements

- [AlphaVantage API](https://www.alphavantage.co/) for stock data.
- [SignalR](https://dotnet.microsoft.com/apps/aspnet/signalr) for real-time communication.
- [Tailwind CSS](https://tailwindcss.com/) for styling.

