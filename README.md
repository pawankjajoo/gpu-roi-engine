# GPU ROI Engine

A sophisticated GPU Return on Investment (ROI) calculator that enables users to evaluate profitability across diverse GPU deployment scenarios—from cryptocurrency mining and cloud computing to AI/ML workloads and data center operations.

## Overview

GPU ROI Engine is a client-side, real-time profitability calculator designed for enterprises, data center operators, and GPU investors. It aggregates live market data from multiple sources and applies advanced algorithms to project accurate ROI calculations without requiring backend infrastructure.

## Features

- **Multi-Use Case Analysis**: Calculate ROI for cryptocurrency mining, cloud GPU leasing, AI inference workloads, and data center deployments
- **Real-Time Market Data**: Live integration with CoinGecko, WhatToMine, and mempool.space for current crypto prices, mining difficulty, and network fees
- **Comprehensive GPU Database**: Support for 40+ GPU models across categories:
  - Enterprise datacenter GPUs (NVIDIA B200, H200, H100, A100)
  - ASIC miners (Bitmain Antminer S-series)
  - Consumer gaming GPUs (RTX 50-series, RTX 40-series)
- **Dynamic Profitability Engine**: Factors in:
  - GPU hashrates and VRAM specifications
  - Mining pool fees (configurable)
  - Electricity costs (user-configurable)
  - Cloud leasing market rates
  - Network transaction fees
  - Hardware MSRP and total cost of ownership
- **Multiple UI Widgets**:
  - Full-page calculator (comprehensive analysis)
  - Ribbon widget (compact, embeddable)
  - Ticker widget (real-time updates)
- **CORS-Safe Architecture**: Requires no backend server; all external APIs use public endpoints with CORS support
- **Wix Integration Ready**: Designed for seamless iframe embedding in web platforms

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Architecture**: Modular widget system with shared data engine
- **APIs**:
  - CoinGecko (cryptocurrency data)
  - WhatToMine (mining profitability)
  - mempool.space (Bitcoin network fees)
  - Vast.ai / RunPod (cloud leasing rates)
- **Deployment**: Client-side only; no backend required

## Files

- `GPU_ROI_Engine.js` - Core profitability calculation engine and GPU database
- `GPU_ROI_Full.html` - Comprehensive full-page calculator widget
- `GPU_ROI_Ribbon.html` - Compact ribbon-style widget for embedding
- `GPU_ROI_Ribbon_Ticker.html` - Ribbon with real-time ticker display
- `GPU_ROI_Ticker.html` - Standalone ticker widget

## Setup & Usage

### Local Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/pawankjajoo/GPU-ROI-ENGINE.git
   cd GPU-ROI-ENGINE
   ```

2. Open any HTML file in a modern web browser:
   ```bash
   # Full-page calculator
   open GPU_ROI_Full.html

   # Or use a local server for CORS compatibility
   python3 -m http.server 8000
   ```

3. Access via browser at `http://localhost:8000/GPU_ROI_Full.html`

### Embedding as Widget

Include the HTML file as an iframe on your website:

```html
<iframe
  src="https://your-domain.com/GPU_ROI_Ribbon.html"
  width="100%"
  height="600"
  frameborder="0"
  allow="clipboard-read; clipboard-write"
></iframe>
```

### Configuration

The calculator adjusts automatically based on user inputs:
- Pool fees (default: 1.5%, user-adjustable)
- Electricity costs (default: $0.12/kWh, user-adjustable)
- Hardware selection from GPU database
- Mining algorithm selection (for applicable hardware)

## How It Works

1. **GPU Selection**: Users select from the comprehensive GPU database
2. **Live Data Fetch**: Engine fetches real-time market data from multiple APIs
3. **ROI Calculation**: Applies profitability algorithm considering:
   - Current crypto prices and block rewards
   - Mining difficulty
   - Network transaction fees
   - Hardware costs and electricity consumption
   - Leasing rates for cloud deployments
4. **Results Display**: Shows projected daily/monthly/yearly returns

## Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (responsive design)

## API Dependencies

- **CoinGecko** - Free tier, no authentication required
- **WhatToMine** - Free tier, no authentication required
- **mempool.space** - Free public API, no authentication required
- **Vast.ai** - Market rate estimates (public data)

All APIs are public with CORS headers enabled for client-side access.

## Roadmap

- [ ] Enhanced historical ROI analysis
- [ ] Portfolio tracking across multiple GPUs
- [ ] Export to PDF/CSV
- [ ] Dark/Light theme toggle
- [ ] Advanced tax calculation tools
- [ ] Integration with hardware monitoring APIs

## License

Proprietary - Pushstart LLC. All rights reserved.

For licensing inquiries or partnership opportunities, contact the repository owner.

## Author

**Pushstart LLC** - Pawan K Jajoo

---

## Screenshots

_Screenshots and demo videos coming soon._

---

## Support & Contributing

For issues, feature requests, or technical questions, please open an issue on GitHub or contact the maintainers.

**Disclaimer**: This calculator provides estimates based on current market conditions. Actual profitability may vary significantly based on market volatility, hardware availability, electricity rates, and other factors. Always conduct your own due diligence before making investment decisions.
