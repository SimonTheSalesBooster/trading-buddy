# The 10-Minute Check-In That Keeps You on the Right Side of Every Trade

> Be the casino, not the gambler. Collect premium. Trade small, trade often.

## The numbers

| Metric | Target |
|--------|--------|
| Monthly return | 3.4% |
| Annualized | 49% |
| Position size | 1% of account |
| Probability of profit | 70% (30 delta) |
| Time in trade | 45 DTE, managed at day 21 |

Most traders check positions reactively.. log in when they feel like it, miss management windows, hold losers too long. Trading Buddy runs a structured daily review. It reads your live spreadsheet, checks market conditions, and tells you exactly what needs attention.

Not an algorithm. Not a bot. The disciplined partner who shows up every day and asks the questions you should be asking yourself.

---

## What you get each morning

### 1. Market regime check
VIX-based. Low vol → credit spreads. High vol → cash-secured puts. No guessing. No "feeling bullish."

### 2. Open position review
Every position checked against your rules:
- Past day 21? Flag it.
- Near short strike? Flag it.
- At 50%+ max profit? Flag it.
- Expired? Flag it immediately.

### 3. Trade suggestions
2-3 specific trades from your watchlist. Only symbols not already in your book. Sized at 1%. With estimated premium, cash required, and return.

### 4. One data-backed observation
Win rate trending down? Holding period creeping past day 21? Sector concentration building? The buddy catches the slow drift before it becomes a drawdown.

---

## The rules

| Rule | Value |
|------|-------|
| Position size | 1% per trade |
| Delta | 30 (70% POP) |
| DTE | 45 days |
| Management | Close at day 21 or 50% profit |
| VIX < 15 | Credit spreads (defined risk) |
| VIX > 15 | CSPs (cash-secured puts) |

---

## Run it

```
/trading-buddy
```

### Setup

1. Google Sheets with tabs: Results, CSP trades, Credit Spreads, Rules
2. Google OAuth credentials in `~/.claude/.env`
3. Copy `trading-buddy.md` to `~/.claude/commands/`
4. Optional: automate with launchd to run before market open

### Resources

- **[Full Options Trading Guide](https://docs.google.com/document/d/1wcsfuWcgfIqCHdttkZfgd3d_odsZCc4FK3XR2M-W_JE/)** — philosophy, math, and mechanics of selling premium

---

## About

Built by Simon Severino... author of Strategy Sprints and Time Freedom with Jay Abraham. Added over $2 Billion in sales to B2B clients in finance, software, and consulting.

One of 47 AI skills available to [Sprint Club](https://www.strategysprints.com) members.

*keep rolling, Simon & The Sprinters*
