# Options Visualizer

A Black-Scholes options pricing tool built as a single standalone HTML file. No build step and no dependencies; just open it in a browser.

Live tool: https://colinwhetstone.github.io/black-scholes-visualizer/

## What it does

**Pricing**
- Black-Scholes closed-form pricing for European calls and puts
- Intrinsic value and time value breakdown
- Moneyness (ITM, ATM, OTM)
- Breakeven price and maximum loss
- Intermediate values: d1, d2, N(d1), N(d2)

**Greeks**
- Delta (Δ): price sensitivity to a move in the underlying
- Gamma (Γ): how fast delta changes
- Theta (Θ): daily time decay in dollars
- Vega (ν): sensitivity to a 1% change in implied volatility

**Charts**
- Payoff diagram at expiry, with the profit zone in green, the loss zone in red, and breakeven marked
- Option price versus implied volatility, with the current IV highlighted

## Inputs

| Input | Description | Default |
|-------|-------------|---------|
| Stock Price (S) | Current underlying price | 100 |
| Strike Price (K) | Option exercise price | 100 |
| Time to Expiry (T) | Years until expiration | 0.5 (182 days) |
| Risk-Free Rate (r) | Annual rate, in % | 5% |
| Implied Volatility (σ) | Annual volatility, in % | 25% |
| Option Type | Call or Put | Call |

## Running it locally

No installation required. Open index.html directly:

```
start index.html      # Windows
open index.html       # macOS
xdg-open index.html   # Linux
```

## Hosted version

The tool runs on GitHub Pages at https://colinwhetstone.github.io/black-scholes-visualizer/
