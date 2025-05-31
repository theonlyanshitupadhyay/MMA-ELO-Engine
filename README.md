# MMA-ELO-Engine
ELO Engine for UFC fighters to give the statistical conclusion of the question "The Greatest Fighter Of All Time"
The MMA-Adapted Elo Rating System

The MMA-adapted Elo rating system evaluates fighter performance through two key mathematical components: the win probability formula and the rating adjustment formula. These have been specifically modified from traditional Elo systems to better reflect MMA's competitive dynamics.

Win Probability Calculation

The probability that Fighter A beats Fighter B is calculated as:
EA = 1 / (1 + 5^(-(RA - RB)/400))

Here, EA represents Fighter A's win probability, while RA and RB denote the fighters' current ratings. The formula uses a base of 5 (instead of chess's 10) to account for MMA's higher unpredictability - a 100-point rating difference translates to approximately a 64% win probability for the favored fighter, compared to chess where this probability would require a 200-point gap.

Rating Adjustment Mechanism

After each bout, ratings are updated using:
Rnew = Rold + K × (S - E)

Where Rnew is the updated rating, Rold the pre-fight rating, K a volatility factor (typically 24-48 in MMA), S the actual result (1 for win, 0.5 for draw, 0 for loss), and E the expected outcome.

Practical Example

Consider Fighter A (1800 rating) versus Fighter B (1700 rating) with K=32:

Expected probability: EA = 1/(1 + 5^(-(1800-1700)/400)) ≈ 0.64

If Fighter A wins:

Their new rating: 1800 + 32 × (1 - 0.64) ≈ 1812

Opponent's new rating: 1700 + 32 × (0 - 0.36) ≈ 1688

This system maintains mathematical elegance while addressing MMA's unique characteristics through:

A steeper probability curve (base 5)

More responsive rating adjustments (higher K-values)

Continuous feedback between expected and actual outcomes

The result is a dynamic yet stable ranking system that appropriately rewards upsets while preserving meaningful long-term skill assessment.
