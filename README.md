# HALO Options Visualizer

A professional Black-Scholes options pricing tool built as a single standalone HTML file. No build step, no server, no dependencies beyond Chart.js.

**Live tool:** [https://colinwhetstone.github.io/options-visualizer](https://colinwhetstone.github.io/options-visualizer)

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

To enable GitHub Pages for this repo:
1. Go to the repository on GitHub → **Settings** → **Pages**
2. Under *Source*, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save** — the site will be live in ~60 seconds

---

## Implementation Notes

- Pure vanilla JavaScript — no frameworks
- Single HTML file with all CSS and JS inline
- Only external dependency: [Chart.js 4.4.1](https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js) from cdnjs
- Font: IBM Plex Mono via Google Fonts
- Assumes European-style options, zero continuous dividend yield
- Normal CDF computed via Abramowitz & Stegun approximation (error < 1.5×10⁻⁷)
