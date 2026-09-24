# econ3916-lab02-deflation
# Deflating Economic Data — Nominal vs. Real

## Objective

This project demonstrates how inflation adjustment separates changes in nominal economic values from changes in their real purchasing power over time.

## Methodology

* Pulled Consumer Price Index data and average hourly earnings from FRED using its public CSV endpoint.
* Built a reusable `deflate_series()` function to convert nominal values into constant 2020 dollars.
* Compared nominal and real average hourly earnings from 1964 through 2026.
* Loaded the Economist's Big Mac Index and filtered the data to the United States.
* Matched semiannual Big Mac observations with the most recent available monthly CPI reading using `.asof()`.
* Calculated nominal, real, and CPI growth rates and built an interactive deflation explorer with a base-year slider.

## Key Findings

Nominal average hourly earnings increased from $2.50 in 1964 to $32.53 in 2026. After adjusting for inflation, the corresponding values were approximately $20.85 and $25.20 in 2020 dollars, showing that the increase in nominal wages is substantially larger than the increase in real purchasing power.

For the U.S. Big Mac, the nominal price increased by approximately 178% over the sample period, while the inflation-adjusted real price increased by approximately 43%. CPI increased by approximately 95% over the same dates. This demonstrates why nominal growth cannot be interpreted as real growth without accounting for changes in the price level.

The interactive explorer also demonstrates that changing the base year changes the dollar level of the real series but does not change its percentage growth rate.
