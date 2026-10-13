UNIFIED SECURITY MASTER - 3 MARKET MOCK DATASET
================================================

All data in this package is synthetic/mock data for project testing.
It is not real market data and should not be presented as real exchange data.

Files:
1) unified_security_master_mock.csv
   - 2,100 securities total
   - 700 NSE + 700 NASDAQ + 700 LSE
   - Mixed security types: Equity, ETF, Mutual Fund, Government Security,
     Corporate Bond, REIT/InvIT-style trust, Money Market

2) market_price_2days_mock.csv
   - Exactly 2 price rows per security
   - 4,200 rows total
   - 2026-10-01 = intended buy date
   - 2026-10-02 = next-day revaluation/date-switch date
   - Day-2 previous_close equals Day-1 close for every security

3) benchmark_2days_mock.csv
   - NSE -> NIFTY 50
   - NASDAQ -> NASDAQ-100
   - LSE -> FTSE 100
   - 2 rows per benchmark

Suggested application behavior:
- Buy on 2026-10-01 using that date's price.
- When UI date changes to 2026-10-02, fetch that date's close_price
  and recalculate current value, allocation, P/L and alerts.
