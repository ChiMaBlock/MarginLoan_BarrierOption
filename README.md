# MarginLoan_BarrierOption
Margin loan is similar to the payoff of leveraged down-and-out barrier call option:    
- The "leveraged" part op the LDAO looks like this. You only pay ($P$) part of the spot price $S_0$ of the underlying asset, the lender provides financing $F_0$ to buy the rest;
- As a buyer, you pay interest $r$ on the financing level $F$;
- The "down-and-out" part is structured as follows. When the price $S$ of the underlying drops below the barrier $B$, the option is cancelled and the underlying asset is sold at the active market price. When the spot price $S_1$ is lower than the financing $F$, your end value is zero. If the spot price is higher than the financing, your payout is $S_1$ - $F_1$ ($F_1$ includes the interest). Your payout cannot be negative.
- The barrier $B$ is increased daily by the amount of the interest on the financing level $F$. So $B_1 = B_0 + F*(1 + i)^t$ or $B_1 = B_0 + F*e^{it}$
- The barrier $B$ is always below the price of the underlying asset, but above the financing level: $S_0 > B > F$
