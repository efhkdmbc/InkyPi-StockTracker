# InkyPi-StockTracker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)

A beautiful stock portfolio tracking plugin for InkyPi that displays real-time market data, portfolio performance, and historical trends on e-ink displays.

![InkyPi Stock Tracker](icon.png)

## ✨ Features

- **Real-time Stock Tracking**: Monitor multiple stocks with live price updates using Yahoo Finance data
- **Portfolio Dashboard**: Visual overview of your complete portfolio with total value and performance
- **Performance Analytics**: Track price changes over customizable time periods (1 day to 1 year)
- **Visual Charts**: Interactive mini-charts showing historical price trends for each stock
- **Best/Worst Performers**: Automatically highlights top and bottom performing stocks
- **Holdings Breakdown**: Detailed view of each position with share count and total value
- **Multi-Asset Support**: Track stocks from various exchanges including US markets and international (e.g., LSE)
- **Flexible Configuration**: Easy-to-use web interface for managing your portfolio

## 📋 Requirements

### Hardware
- Raspberry Pi (any model with network connectivity)
- InkyPi-compatible e-ink display
- InkyPi framework installed and configured

### Software Dependencies
- Python 3.7 or higher
- InkyPi plugin framework
- Required Python packages:
  - `yfinance` - Stock market data retrieval
  - `matplotlib` - Chart generation
  - `numpy` - Numerical computations
  - `Pillow (PIL)` - Image processing

## 🚀 Installation

### 1. Install InkyPi Framework
First, ensure you have InkyPi installed on your Raspberry Pi. Refer to the [InkyPi documentation](https://github.com/MEANGAIN/InkyPi) for setup instructions.

### 2. Clone this Repository
```bash
cd /path/to/inkypi/plugins/
git clone https://github.com/MEANGAIN/InkyPi-StockTracker.git stocktracker
```

### 3. Install Dependencies
```bash
pip install yfinance matplotlib numpy Pillow
```

### 4. Register the Plugin
The plugin should be automatically detected by InkyPi. If not, restart the InkyPi service:
```bash
sudo systemctl restart inkypi
```

## 📖 Usage

### Configuration

1. Access the InkyPi web interface (typically at `http://your-pi-ip:5000`)
2. Navigate to the Stock Tracker plugin
3. Configure your portfolio:

   **Stock Tickers**: Enter comma-separated stock symbols (e.g., `AAPL, MSFT, TSLA, 0P0001RU1X.L`)
   
   **Number of Shares**: Enter corresponding share counts (e.g., `10, 5, 3, 152.2`)
   
   **Time Period**: Select the time range for calculating changes:
   - 1 Day
   - 5 Days
   - 1 Month
   - 3 Months
   - 6 Months
   - 1 Year
   - Year to Date

4. Click "Update Now" to display immediately or "Add to Playlist" to include in rotation

### Example Configuration

```
Tickers: AAPL, GOOGL, MSFT, TSLA
Shares: 10, 5, 15, 3
Period: 1mo
```

This will track:
- 10 shares of Apple (AAPL)
- 5 shares of Google (GOOGL)
- 15 shares of Microsoft (MSFT)
- 3 shares of Tesla (TSLA)

All changes calculated over a 1-month period.

### International Stocks

The plugin supports international exchanges. Use the appropriate ticker format:
- **US Stocks**: Standard ticker (e.g., `AAPL`)
- **London Stock Exchange**: Use format like `0P0001RU1X.L`
- Refer to [Yahoo Finance](https://finance.yahoo.com/) for correct ticker symbols

## 🎨 Dashboard Components

The generated dashboard includes:

1. **Individual Stock Cards** (Best/Worst Performers)
   - Stock symbol and name
   - Current price
   - Price change (amount and percentage)
   - Mini price history chart
   - Holdings information

2. **Portfolio Value Chart**
   - Historical portfolio value over selected period
   - Visual trend line with color-coded performance
   - Total change indicator

3. **Portfolio Summary**
   - Total portfolio value
   - Overall performance (change amount and percentage)
   - Complete holdings breakdown with percentages

## 🛠️ Platform Compatibility

- **Operating System**: Raspberry Pi OS (Raspbian), Linux
- **Python Version**: 3.7+
- **Display**: InkyPi-compatible e-ink displays
- **Network**: Internet connection required for stock data retrieval

## ⚠️ Disclaimer

**IMPORTANT**: This software is provided for **informational and educational purposes only**. It is **NOT** intended to be financial, investment, trading, or legal advice.

- Market data is obtained from third-party sources (Yahoo Finance) and may be delayed, inaccurate, or incomplete
- Past performance does not guarantee future results
- The authors and contributors make no representations or warranties regarding the accuracy, reliability, or suitability of the information displayed
- No liability is accepted for any losses or damages arising from the use of this software
- **Use this software entirely at your own risk**

Always consult with qualified financial professionals before making investment decisions.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2026 MEANGAIN

## 👤 Author

**MEANGAIN**

- GitHub: [@MEANGAIN](https://github.com/MEANGAIN)
- Repository: [InkyPi-StockTracker](https://github.com/MEANGAIN/InkyPi-StockTracker)

## 🔗 Related Projects

- [InkyPi Framework](https://github.com/MEANGAIN/InkyPi) - The core plugin framework for Raspberry Pi e-ink displays

## 📝 Version History

- **v1.0.0** - Initial release with portfolio tracking and dashboard visualization

---

*Made with ❤️ for the Raspberry Pi and e-ink display community* 
