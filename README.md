# 🎲 Crypto Casino House Edge Calculator

An open-source tool to calculate the true house edge, RTP, and expected loss for crypto casino games.

🖥 [Use the Live Tool](https://gamblingbitcoin.github.io/crypto-casino-house-edge-calculator/) | 📖 [Learn About House Edge](https://btcgambling.com/house-edge-calculator/)

## What Is House Edge?

House edge is the mathematical advantage the casino has on every bet you place. It's the percentage of each wager that the casino expects to keep over time.

For example, a 1% house edge means:
- For every **$100 wagered**, the casino keeps **$1** on average
- Your **Return to Player (RTP)** is **99%**
- Over 1,000 bets of $1 each, your expected loss is **$10**

A lower house edge means better odds for the player. This tool lets you calculate the exact edge for any game parameters.

## Supported Games

| Game | What You Enter | What You Learn |
|------|---------------|----------------|
| 🎲 Classic Dice | Win chance + payout multiplier | True edge vs. fair payout |
| 🚀 Crash / Limbo | Casino commission + cash-out target | Edge from commission, win probability |
| 🎡 Roulette | Wheel type (European/American/Custom) | Edge from zero slots |
| 🃏 Blackjack | Decks, dealer rules, BJ payout | Approximate edge from ruleset |
| 📍 Plinko | Stated RTP | Verify the claimed edge |
| 🎰 Slots | Stated RTP + spins per session | Expected cost of a session |

## How to Use

### Online

Visit the [live tool](https://gamblingbitcoin.github.io/crypto-casino-house-edge-calculator/) — no installation needed.

### Locally

1. Clone this repository: `git clone https://github.com/gamblingbitcoin/crypto-casino-house-edge-calculator.git`
2. Open `index.html` in your browser
3. Select a game type from the tabs
4. Enter the casino's parameters
5. Read the house edge, RTP, and expected loss

## Calculations Explained

### Dice

```
Fair payout = 1 / (win chance / 100)
House edge = (1 - actual payout / fair payout) × 100
```

Example: 50% win chance with 1.98× payout → fair payout is 2.00× → edge is 1.00%

### Crash / Limbo

```
House edge ≈ commission percentage
Win probability = (1 - commission / 100) / target × 100
```

The commission is taken from the prize pool each round, making it a direct house edge.

### Roulette

```
House edge = zero slots / total slots × 100
```

- European (1 zero, 37 slots): 2.70%
- American (2 zeros, 38 slots): 5.26%

### Blackjack

The calculator uses a base edge model adjusted for:
- Number of decks (fewer decks = lower edge)
- Dealer hits soft 17 (adds ~0.22%)
- 6:5 blackjack payout (adds ~1.39%)

### Slots & Plinko

For these games, the RTP is set by the game provider. Enter the stated RTP to see the real cost of playing.

## Typical House Edges

| Game | Typical Edge | RTP |
|------|-------------|-----|
| Dice (1% edge) | 1.00% | 99.00% |
| Crash (1% fee) | 1.00% | 99.00% |
| Blackjack (8D S17 3:2) | 0.46% | 99.54% |
| European Roulette | 2.70% | 97.30% |
| American Roulette | 5.26% | 94.74% |
| Plinko (typical) | 1.00% | 99.00% |
| Slots (typical) | 4.00% | 96.00% |

## Resources

- [What Is House Edge? — Complete Guide](https://btcgambling.com/house-edge-calculator/) — Detailed explanation with examples
- [Bitcoin Dice Strategies](https://btcgambling.com/bitcoin-dice-strategies/) — Optimize your dice play
- [Provably Fair Verifier](https://gamblingbitcoin.github.io/provably-fair-verifier/) — Verify crypto casino game results

## Contributing

Contributions are welcome! If you'd like to add support for another game type or improve the calculations, please open a pull request.

## License

MIT License — see [LICENSE](LICENSE) for details.

---

Built and maintained by [BtcGambling.com](https://btcgambling.com) — Independent crypto gambling resource 🎰
