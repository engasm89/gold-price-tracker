# Gold Price Tracker & Alert System

A real-time gold (XAU/USD) price tracking dashboard with email and Telegram alert capabilities.

## Features

- **Multi-timeframe Monitoring**: Track gold prices across 5 minutes, 15 minutes, and 1 hour sessions
- **Real-time Updates**: Continuous price monitoring with configurable refresh rates
- **Alert System**: Get notified when gold prices move ≥500 pips ($50 per ounce)
- **Email Alerts**: Receive email notifications at configured addresses
- **Telegram Integration**: Get instant alerts via Telegram bot
- **Visual Dashboard**: Beautiful dark-themed interface with:
  - Live price cards showing session high/low/open
  - Movement tracker with progress bars
  - Alert history log
  - Price change visualization
- **Export Data**: Download alert history as CSV

## Getting Started

### Option 1: Direct Usage

Simply open `index.html` in your browser to start using the dashboard.

### Option 2: Local Server (Recommended)

For better performance and to avoid CORS issues:

```bash
# Using Python 3
python -m http.server 8000

# Or using Python 2
python -m SimpleHTTPServer 8000

# Or using Node.js http-server
npx http-server
```

Then navigate to `http://localhost:8000`

## Configuration

### Email Alerts

1. Open the dashboard
2. Go to "Alert Configuration" panel
3. Enter your email address
4. Click "Save Settings"

### Telegram Alerts

1. Create a bot with [@BotFather](https://t.me/BotFather)
2. Get your bot token
3. Get your chat ID (use [@userinfobot](https://t.me/userinfobot))
4. Enter both in the configuration panel
5. Click "Save Settings"

## Technical Details

- **Pip Value**: $0.10 (1 pip = $0.10 per ounce)
- **Alert Threshold**: 500 pips = $50 per ounce (default, configurable)
- **Supported Timeframes**: 5 minutes, 15 minutes, 1 hour
- **Refresh Rates**: 1, 2, or 5 minutes (configurable)

## API Integration

For production use, integrate with one of these APIs:

- **MetalpriceAPI**: https://metalpriceapi.com
- **Metals.dev**: https://api.metals.dev/v1/latest
- **GoldPriceZ API**: https://goldpricez.com/api
- **Twelve Data**: https://twelvedata.com

Current implementation uses simulated data for demonstration.

## Browser Notifications

The dashboard requests browser notification permission to show desktop alerts when thresholds are reached.

## License

MIT License

## Author

Created by engasm89

