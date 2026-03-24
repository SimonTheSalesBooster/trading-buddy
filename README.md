# Trading Buddy: Your Daily 10-Minute Options Check-In

> Be the casino, not the gambler. Collect premium. Trade small, trade often.

## The core idea

Most traders check their positions reactively — they log in when they feel like it, miss management windows, and hold losers too long. The Trading Buddy fixes this by running a structured 10-minute daily check-in that reads your live spreadsheet, checks market conditions, and tells you exactly what needs attention.

It's not an algorithm. It's not a bot that trades for you. It's the disciplined trading partner who shows up every single day, reads the data, and asks the questions you should be asking yourself.

---

## The Skill: [trading-buddy.md](trading-buddy.md)

A structured daily options trading review that works with any frontier AI model. Designed to integrate with Google Sheets, market data, and Slack.

Add `trading-buddy.md` to your project as a skill file or system prompt.

---

## What You Get

### 1. Market Regime Check

VIX-based regime detection. The buddy reads the current VIX and tells you whether to favor credit spreads (low vol) or cash-secured puts (high vol). No guessing. No "feeling bullish."

### 2. Open Position Review

Every open position reviewed against your rules:
- Past day 21? Flag it.
- Near your short strike? Flag it.
- At 50%+ of max profit? Flag it.
- Expired? Flag it immediately.

The buddy catches what you'd miss scanning a spreadsheet at 6am.

### 3. Trade Suggestions

2-3 specific trades from your pre-trade plan watchlist:
- Only symbols not already in your book
- Sized at 1% of account
- 30 delta, 45 DTE
- With estimated premium, cash required, and return

### 4. Trading Plan Improvement

One data-backed observation per day. Win rate trending down? Holding period creeping past day 21? Concentration in one sector? The buddy catches the slow drift before it becomes a drawdown.

---

## The Philosophy

This system is built for **selling options premium** — specifically cash-secured puts and put credit spreads. The rules:

| Rule | Value |
|------|-------|
| Position size | 1% of account per trade |
| Delta | 30 (70% probability of profit) |
| DTE | 45 days to expiration |
| Management | Close at day 21 or at 50% profit |
| VIX < 15 | Favor credit spreads (defined risk) |
| VIX > 15 | Favor CSPs (cash-secured puts) |
| Target | 3.4% monthly / 49% annualized |

---

## Setup

1. **Create your spreadsheet** — Use Google Sheets with tabs for Results, CSP trades, Credit Spreads, and Rules. See the skill file for the exact column structure.
2. **Configure API access** — You need Google OAuth credentials with Sheets API access. Store them in `~/.claude/.env`.
3. **Add the skill** — Copy `trading-buddy.md` to `~/.claude/commands/` and run `/trading-buddy`.
4. **Optional: Automate** — Set up a launchd agent (macOS) or cron job to run daily before market open.

---

## Resources

- **[Full Options Trading Guide](https://docs.google.com/document/d/1wcsfuWcgfIqCHdttkZfgd3d_odsZCc4FK3XR2M-W_JE/)** — Step-by-step guide for beginners. Covers the philosophy, the math, and the mechanics of selling options premium.

---

## Part of the Strategy Sprints Method

This skill is one of 47 AI skills available to [Sprint Club](https://www.strategysprints.com) members. Built for founders who want to build repeatable systems — for business and for investing.
