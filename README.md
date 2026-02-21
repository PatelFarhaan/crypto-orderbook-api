# Circle Again

A lightweight REST API that retrieves real-time Bitcoin (BTC/USDT) order book data from the Binance exchange, exposing current ask and bid prices with quantities.

## Tech Stack

- **Language:** Python 3.8+
- **Framework:** Flask
- **Exchange Library:** CCXT (CryptoCurrency eXchange Trading Library)

## Features

- Real-time BTC/USDT order book retrieval from Binance
- RESTful API endpoint returning structured ask/bid data
- JSON response format with price and quantity breakdowns

## Prerequisites

- Python 3.8 or higher
- pip

## Installation & Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd circle_again
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Copy the environment file and configure:
   ```bash
   cp .env.example .env
   ```

## Environment Variables

| Variable      | Description              | Default       |
|---------------|--------------------------|---------------|
| `FLASK_ENV`   | Flask environment mode   | `development` |
| `FLASK_DEBUG` | Enable debug mode        | `1`           |
| `FLASK_PORT`  | Port to run the server   | `5000`        |

## How to Run

```bash
python main.py
```

The server will start at `http://127.0.0.1:5000`.

## API Endpoints

| Method | Endpoint    | Description                            |
|--------|-------------|----------------------------------------|
| GET    | `/spending` | Returns BTC/USDT order book (asks/bids)|

### Example Response

```json
{
  "result": true,
  "data": {
    "asks": [{"price": 50000.0, "quantity": 0.5}],
    "bids": [{"price": 49999.0, "quantity": 1.2}]
  }
}
```

## Project Structure

```
circle_again/
├── main.py             # Application entry point and API routes
├── requirements.txt    # Python dependencies
├── .env.example        # Environment variable template
├── .gitignore          # Git ignore rules
├── Dockerfile          # Container configuration
├── Makefile            # Common development commands
└── README.md           # Project documentation
```

## License

MIT License
