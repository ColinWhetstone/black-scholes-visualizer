# Options Visualizer

A Black-Scholes options pricing tool built as a single standalone HTML file.

**Live tool:** https://colinwhetstone.github.io/black-scholes-visualizer/
---

## Features

**Pricing**
- Black-Scholes closed-form pricing for European calls and puts
- Intrinsic value / time value decomposition
- Moneyness classification (ITM / ATM / OTM)
- Breakeven price and maximum loss
- d₁, d₂, N(d₁), N(d₂) intermediate values

**Greeks**
- Delta (Δ) — price sensitivity to underlying move
- Gamma (Γ) — rate of change of delta
- Theta (Θ) — daily time decay in dollars
- Vega (ν) — sensitivity to 1% change in implied volatility

**Charts**
- Payoff diagram at expiry — profit zone in green, loss zone in red, breakeven marked
- Option price vs implied volatility curve — with current IV highlighted

---

## Inputs

| Input | Description | Default |
|-------|-------------|---------|
| Stock Price (S) | Current underlying price | 100 |
| Strike Price (K) | Option exercise price | 100 |
| Time to Expiry (T) | Years until expiration | 0.5 (182d) |
| Risk-Free Rate (r) | Annual rate in % | 5% |
| Implied Volatility (σ) | Annual volatility in % | 25% |
| Option Type | Call or Put toggle | Call |

---

## Opening Locally

No installation required. Open directly in any browser:

```
# Option 1: double-click index.html in File Explorer

# Option 2: open from terminal
start index.html          # Windows
open index.html           # macOS
xdg-open index.html       # Linux
```

---

## Hosted on GitHub Pages

This tool is hosted at:

**[https://colinwhetstone.github.io/options-visualizer](https://colinwhetstone.github.io/options-visualizer)**


