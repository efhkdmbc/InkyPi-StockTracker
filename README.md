# InkyPi-StockTracker

A portfolio tracking plugin for InkyPi that displays stock market data in an interactive dashboard format.


## Description

InkyPi-StockTracker retrieves real-time stock market data using yfinance and renders a comprehensive visual dashboard showing:
- Stock performance for multiple tickers
- Portfolio value and historical trends
- Price changes and percentage gains/losses
- Holdings breakdown with individual stock positions
- Visual charts showing price history over customizable time periods

## Installation

Install the plugin using the InkyPi CLI, providing the plugin ID and GitHub repository URL:

```bash
inkypi plugin install stocktracker https://github.com/efhkdmbc/InkyPi-StockTracker
```

## Dependencies

This plugin requires the following Python packages:
- **yfinance** - For fetching stock market data from Yahoo Finance
- **matplotlib** - For creating charts and visualizations
- **numpy** - For numerical calculations
- **Pillow (PIL)** - For image generation and manipulation

These dependencies are automatically installed when you install the plugin.

## API Information

### Data Source
This plugin uses **yfinance**, which retrieves data from Yahoo Finance.

- **API Key Required:** No - yfinance does not require an API key
- **Usage Limits:** Yahoo Finance may rate-limit requests if too many are made in a short period. Normal plugin usage (refreshing every few minutes to hours) should not encounter rate limits.
- **Cost:** Free - no charges for data access
- **Data Quality:** Market data may be delayed by 15-20 minutes for some exchanges. Real-time data availability varies by stock and exchange.

### Supported Ticker Formats
- US stocks: `AAPL`, `MSFT`, `TSLA`
- International stocks: Include exchange prefix (e.g., `0P0001RU1X.L` for LSE)

## Configuration

When adding the plugin to your playlist, configure:

1. **Stock Tickers** - Comma-separated list of stock symbols (e.g., `AAPL, MSFT, TSLA`)
2. **Number of Shares** - Comma-separated list of share quantities matching the ticker order (e.g., `10, 5, 3`)
3. **Time Period** - Historical period for calculating price changes:
   - 1 Day
   - 5 Days
   - 1 Month (recommended for general tracking)
   - 3 Months
   - 6 Months
   - 1 Year
   - Year to Date

## Development Status

**Status:** Active Development

This plugin is actively maintained and open to contributions. If you encounter issues or have feature requests, please open an issue on the [GitHub repository](https://github.com/efhkdmbc/InkyPi-StockTracker/issues).


## ⚠️ Disclaimer

**IMPORTANT**: This software is provided for **informational and educational purposes only**. It is **NOT** intended to be financial, investment, trading, or legal advice.

- Market data is obtained from third-party sources (Yahoo Finance) and may be delayed, inaccurate, or incomplete
- Past performance does not guarantee future results
- The authors and contributors make no representations or warranties regarding the accuracy, reliability, or suitability of the information displayed
- No liability is accepted for any losses or damages arising from the use of this software
- **Use this software entirely at your own risk**

Always consult with qualified financial professionals before making investment decisions.
This software is provided for informational and educational purposes only. It is NOT intended to be financial, investment, trading, or legal advice. Market data is obtained from third-party sources and may be delayed, inaccurate, or incomplete.

The authors and contributors make no representations or warranties of any kind regarding the accuracy, reliability, or suitability of the information displayed and accept no liability for any losses or damages arising from its use. Use this software entirely at your own risk.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**MEANGAIN**

- GitHub: [@MEANGAIN](https://github.com/MEANGAIN)
- Repository: [InkyPi-StockTracker](https://github.com/MEANGAIN/InkyPi-StockTracker)

## 🔗 Related Projects

- [InkyPi Framework](https://github.com/fatihak/InkyPi) - The core plugin framework for Raspberry Pi e-ink displays

## 📝 Version History

- **v1.0.0** - Initial release with portfolio tracking and dashboard visualization

---

*Made with ❤️ for the Raspberry Pi and e-ink display community* 
