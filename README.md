# Avellaneda-Stoikov-Model

## Replicationof High-Frequency Trading in a Limit Order Book
This repository cotains my implementation of the model from the paper High-Frequency Trading in a Limit Order Book.

### Resources
Three PDFs are provided for reference:
1. The 1st edition of the paper
2. The 2nd edition of the paper
3. A PPT with detailed mathematical derivations
Note on discrepencies: All three documents contain minor mathematical errors in the proofs. The PPT is the most comprehensive but omits a denominator of 2 in equations (21) and (22).

### Strategy Implementation
The paper compares two strategies:
1. Inventory Strategy: Spread is dynamic and decreasing and centered around the reservation price.
2. Symmetric Strategy: Described as using the same spread as the inventory strategy but centered around the mid_price instead.

Key observations: The paper's table shows fixed spreads for both strategies (equal to the second term of the spread equation). To reconcile this, I tested two approaches:
1. Dynamic spreads: Inventory strategy (reservation price-centered) vs symmetric strategy (mid-price centered).
2. Fixed spread for symmetric strategy: Only depends on gamma and k.
Result: The fixed-spread approach yields results more consistent with the paper.

### Future Rearch 1: Parmeter Estimation
The current model relies on predefined parameters derived from an idealized mathematical framework. However, real-world market microstructure may deviate from these assumptions, and esimation errors could significantly impact model performance.
Key considerations includes:
1. ​Empirical calibration: Estimating parameters (e.g., order arrival rates, volatility) from actual market data to better reflect observed dynamics.
2. ​Robustness testing: Quantifying how model performance degrades under parameter misspecification or noisy estimates.
3. ​Adaptive strategies: Developing methods to dynamically adjust parameters in response to changing market conditions.

### Future Rearch 2: Latency Effects
The current model assumes zero latency--orders are executed immediately with the perfect price/inventory visiblily. A natural extension would be to study how latency impacts strategy performance, including:
1. Delays in price updates or order execution.
2. Effects on inventory management and spread adjustments.

