Global Macroeconomic Cycle Model — Full Specification
1. Objective
Build a monthly global macroeconomic cycle model that classifies the world economy into actionable regimes using real-economy, monetary, credit, inflation, liquidity, and market indicators.
The model should answer three practical questions:
1.	Where are we in the global cycle?
Expansion, late-cycle, slowdown, contraction, recovery, stagflation, reflation, or disinflationary easing.
2.	What is driving the regime?
Growth momentum, inflation pressure, policy stance, credit stress, liquidity, or market risk appetite.
3.	How should a diversified portfolio interpret the regime?
Risk-on/risk-off tilt, equity vs. bonds, duration exposure, credit exposure, commodities, gold, USD, emerging markets, and cash.
This is not a trading signal by itself. It is a macro allocation framework that converts economic data into a regime map.
 
2. Economic Theory Behind the Model
The model combines five macro-financial theories:
2.1 Business Cycle Theory
Economic activity moves through recurring phases:
Phase	Growth	Inflation	Policy	Credit	Market Behavior
Recovery	Improving	Low/stable	Easy	Stabilizing	Risk assets recover
Expansion	Strong	Moderate	Neutral/tightening	Healthy	Equities and credit perform
Late Cycle	Strong but slowing	High/rising	Tight	Deteriorating	Commodities/value may outperform
Slowdown	Falling	Mixed	Tight or easing	Weakening	Defensive assets improve
Contraction	Negative	Usually falling	Easing	Stress	Bonds/cash/gold favored
Reflation	Rising	Rising from low base	Easy	Improving	Cyclicals, EM, commodities
Stagflation	Weak	High	Constrained	Deteriorating	Difficult regime; gold/commodities/cash often useful
2.2 Yield Curve and Monetary Transmission
The yield curve embeds market expectations about future short rates, inflation, and growth. A steep curve usually indicates future recovery or reflation; an inverted curve often reflects restrictive policy and recession risk.
This connects directly with fixed-income theory: the term structure of interest rates compares yields across maturities while holding other bond characteristics constant. Your fixed-income materials emphasize that yield differences can arise from maturity, currency, credit risk, liquidity, tax status, and coupon structure, so the model should use comparable sovereign yield data wherever possible.  
2.3 Credit Cycle Theory
Credit conditions amplify the business cycle. When credit spreads tighten, lending conditions ease and risk appetite improves. When spreads widen, default risk and liquidity stress increase.
Your fixed-income materials frame credit spreads as a combination of liquidity premium plus credit spread, and emphasize that spreads tend to narrow as the cycle improves and widen when the cycle deteriorates.  
2.4 Inflation and Real Rate Dynamics
Inflation regimes determine central-bank reaction functions. The key is not only whether inflation is high, but whether it is accelerating or decelerating relative to trend.
Important distinction:
•	Growth falling + inflation falling → classic slowdown/disinflation.
•	Growth falling + inflation rising → stagflation.
•	Growth rising + inflation rising → reflation or late-cycle overheating.
•	Growth rising + inflation falling → goldilocks/recovery.
2.5 Market-Based Forward-Looking Signals
Markets often price macro inflection points before hard economic data confirms them. Therefore, the model includes:
•	Equity momentum
•	Credit spreads
•	Yield curve slope
•	Volatility
•	Commodity momentum
•	USD strength
•	Emerging market relative performance
This matters because hard macro data is often lagged or revised.
________________________________________
3. Model Architecture
The model should have four main sub-scores:
Sub-score	Purpose	Direction
Growth Score	Measures real economic momentum	Higher = stronger growth
Inflation Score	Measures inflation pressure	Higher = more inflationary
Policy & Liquidity Score	Measures monetary/financial conditions	Higher = easier conditions
Risk & Credit Score	Measures market stress and credit risk	Higher = healthier risk appetite
Then build:
Global Macro Cycle Score =
0.35 × Growth Score
+ 0.20 × Policy & Liquidity Score
+ 0.25 × Risk & Credit Score
− 0.20 × Inflation Stress Score
Separate from that, classify the regime using a two-axis system:
Growth Momentum Axis = Growth Score

Inflation Pressure Axis = Inflation Score
Then use credit/liquidity stress as an overlay.
________________________________________
4. Indicator Categories
The model should include the following categories:
1.	Real Economic Activity
2.	Labor Market
3.	Inflation
4.	Monetary Policy
5.	Yield Curve
6.	Credit Conditions
7.	Liquidity and Financial Stress
8.	Money and Credit Growth
9.	External Sector / Global Trade
10.	Market-Based Risk Appetite
11.	Commodities
12.	Global and Regional Forecasts
________________________________________
5. Exact Indicators, Sources, Timing, Frequency, and Transformation
5.1 Real Economic Activity
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
Global real GDP growth	IMF WEO / World Bank	Coincident / lagging	Quarterly/Annual	YoY %, interpolate to monthly carefully	Higher = stronger
U.S. Industrial Production	FRED	Coincident	Monthly	YoY %, 3M annualized change	Higher = stronger
Euro Area Industrial Production	OECD / Eurostat	Coincident	Monthly	YoY %, 3M momentum	Higher = stronger
China Industrial Production	World Bank / OECD / national source	Coincident	Monthly	YoY %, 3M momentum	Higher = stronger
Global Manufacturing PMI	S&P Global, if licensed; alternative OECD CLI	Leading	Monthly	Level minus 50; 3M change	Higher = stronger
OECD Composite Leading Indicator	OECD	Leading	Monthly	Level gap from 100; 3M change	Higher = stronger
The OECD defines the Composite Leading Indicator as an index designed to provide early signals of turning points in business cycles around long-term potential activity.  
5.2 Labor Market
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
U.S. unemployment rate	FRED	Lagging	Monthly	Level, 3M change	Lower = stronger
U.S. payroll growth	FRED	Coincident	Monthly	3M average monthly change	Higher = stronger
Initial jobless claims	FRED	Leading	Weekly → monthly	4W average, YoY %, inverted score	Lower = stronger
Global unemployment	World Bank / IMF	Lagging	Annual	YoY change, country-weighted	Lower = stronger
Employment-to-population ratio	FRED / OECD	Coincident	Monthly/Quarterly	Level z-score	Higher = stronger
5.3 Inflation
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
U.S. CPI YoY	FRED	Coincident / lagging	Monthly	YoY %, 3M annualized	Higher = inflationary
U.S. Core CPI YoY	FRED	Coincident / lagging	Monthly	YoY %, 3M annualized	Higher = inflationary
U.S. PCE inflation	FRED	Coincident	Monthly	YoY %, 3M annualized	Higher = inflationary
Global CPI inflation	World Bank / IMF	Lagging	Annual/Monthly where available	YoY %, country-weighted	Higher = inflationary
Producer Price Index	FRED / OECD	Leading/coincident	Monthly	YoY %, 3M momentum	Higher = inflationary
Commodity index YoY	FRED / Yahoo Finance / World Bank Pink Sheet	Leading	Monthly	YoY %, 6M momentum	Higher = inflationary
5Y5Y inflation expectations	FRED	Leading	Daily → monthly	Monthly average, 3M change	Higher = inflationary
5.4 Monetary Policy
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
Fed Funds Effective Rate	FRED	Coincident	Daily → monthly	Level, 3M change	Higher = tighter
ECB policy rate	ECB Data Portal / FRED	Coincident	Daily/monthly	Level, 3M change	Higher = tighter
Global policy-rate average	BIS / central banks / IMF	Coincident	Monthly/Quarterly	GDP-weighted level and 6M change	Higher = tighter
Real policy rate	FRED + CPI/PCE	Coincident	Monthly	Policy rate − inflation YoY	Higher = tighter
Shadow policy rate	Academic/optional	Coincident	Monthly	Level z-score	Higher = tighter
FRED’s API is suitable for retrieving full economic time-series histories programmatically from the FRED database.  
5.5 Yield Curve
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
U.S. 10Y − 2Y Treasury spread	FRED	Leading	Daily → monthly	Monthly average, level	Higher = easier/recovery
U.S. 10Y − 3M Treasury spread	FRED	Leading	Daily → monthly	Monthly average, level	Higher = easier/recovery
Global yield-curve slope	OECD / BIS / national sources	Leading	Monthly	GDP-weighted 10Y−2Y	Higher = easier/recovery
Real 10Y yield	FRED	Coincident	Daily → monthly	Level, 3M change	Higher = tighter
Term premium	NY Fed / FRED if available	Leading	Monthly	Level, z-score	Higher = tighter long-end compensation
5.6 Credit Conditions
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
U.S. investment-grade OAS	FRED / ICE BofA	Leading/coincident	Daily → monthly	Spread level, 3M change, inverted	Lower = healthier
U.S. high-yield OAS	FRED / ICE BofA	Leading	Daily → monthly	Spread level, 3M change, inverted	Lower = healthier
Emerging market sovereign spread	J.P. Morgan EMBI if available / FRED proxies	Leading	Daily → monthly	Spread level, 3M change, inverted	Lower = healthier
Bank lending standards	FRED SLOOS	Leading	Quarterly	Level, change, inverted	Lower tightening = healthier
Corporate default rate	Moody’s/S&P, optional	Lagging	Monthly/Quarterly	Level, 12M change, inverted	Lower = healthier
Credit-to-GDP gap	BIS	Leading	Quarterly	Level, z-score, risk overlay	Moderate = healthy; extreme = vulnerability
BIS defines the credit-to-GDP gap as the difference between the credit-to-GDP ratio and its long-run trend; it is used as a reference indicator under Basel III for countercyclical capital buffers.  
5.7 Liquidity and Financial Stress
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
Chicago Fed National Financial Conditions Index	FRED	Leading/coincident	Weekly → monthly	Level, inverted	Lower stress = healthier
St. Louis Fed Financial Stress Index	FRED	Leading/coincident	Weekly → monthly	Level, inverted	Lower stress = healthier
TED spread / funding spread proxy	FRED	Leading	Daily → monthly	Level, 3M change, inverted	Lower = healthier
SOFR / repo stress indicators	FRED / NY Fed	Leading	Daily → monthly	Level, spikes, z-score	Lower = healthier
VIX	FRED / Cboe	Leading	Daily → monthly	Level, 3M change, inverted	Lower = risk-on
FRED carries the CBOE Volatility Index series as daily, not seasonally adjusted data, and Cboe also provides historical VIX data.  
5.8 Money and Credit Growth
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
U.S. M2 money supply	FRED	Leading/coincident	Monthly	YoY %, real M2 YoY	Higher = easier
Bank credit growth	FRED	Coincident	Weekly/monthly	YoY %, 3M momentum	Higher = stronger
Global broad money growth	World Bank / IMF	Coincident	Annual/monthly where available	YoY %, GDP-weighted	Higher = easier
Private credit growth	BIS	Leading/coincident	Quarterly	YoY %, credit gap	Higher = stronger but excessive = risk
Debt service ratio	BIS	Leading risk indicator	Quarterly	Level, z-score, inverted	Lower burden = healthier
BIS describes debt service ratios as the share of income used to service debt for households, non-financial corporations, and the total private non-financial sector; BIS also characterizes the series as an early warning indicator for systemic banking crises.  
5.9 External Sector and Global Trade
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
World trade volume	CPB World Trade Monitor / World Bank	Coincident	Monthly	YoY %, 3M momentum	Higher = stronger
Export growth by region	World Bank / OECD	Coincident	Monthly/Quarterly	YoY %, 3M momentum	Higher = stronger
Current account balance	IMF / World Bank	Lagging	Quarterly/Annual	% of GDP, change	Context-specific
FX reserve growth	IMF / World Bank	Coincident	Monthly/Quarterly	YoY %, 6M momentum	Higher = external resilience
Dollar index	FRED / Yahoo Finance	Leading/coincident	Daily → monthly	3M and 6M return, inverted for global liquidity	Lower USD = easier global liquidity
5.10 Market-Based Risk Appetite
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
MSCI ACWI ETF proxy: ACWI	Yahoo Finance / yfinance	Leading	Daily → monthly	3M/6M total return	Higher = risk-on
S&P 500 ETF: SPY	Yahoo Finance / yfinance	Leading	Daily → monthly	3M/6M return	Higher = risk-on
Emerging markets ETF: EEM	Yahoo Finance / yfinance	Leading	Daily → monthly	3M/6M return, relative to ACWI	Higher = global risk-on
High yield ETF: HYG	Yahoo Finance / yfinance	Leading	Daily → monthly	3M/6M return, spread proxy	Higher = risk-on
Investment-grade ETF: LQD	Yahoo Finance / yfinance	Coincident	Daily → monthly	3M/6M return	Higher = credit healthy
Long Treasury ETF: TLT	Yahoo Finance / yfinance	Defensive signal	Daily → monthly	3M/6M return	Higher = duration bid
Gold ETF: GLD	Yahoo Finance / yfinance	Defensive/inflation hedge	Daily → monthly	3M/6M return	Context-specific
Commodity ETF: DBC	Yahoo Finance / yfinance	Inflation/reflation	Daily → monthly	3M/6M return	Higher = reflation/inflation
For official macroeconomic indicators, use official APIs first; for market ETF proxies, Yahoo Finance through yfinance is practical, but it should be treated as a convenience data layer rather than a fully institutional-grade market data source.
5.11 Forecasts and Global Macro Expectations
Indicator	Preferred Source	Cycle Type	Frequency	Transformation	Direction
IMF WEO real GDP forecast	IMF DataMapper / IMF Data API	Leading	Semiannual/quarterly updates	Forecast revision, next-year GDP growth	Higher = stronger
IMF WEO inflation forecast	IMF DataMapper / IMF Data API	Leading	Semiannual/quarterly updates	Forecast revision, next-year inflation	Higher = inflationary
IMF fiscal balance forecast	IMF WEO	Policy/fiscal	Semiannual/quarterly	% of GDP, revision	Larger deficit = stimulus/risk
IMF government debt forecast	IMF WEO	Structural risk	Semiannual/quarterly	% of GDP, change	Higher debt = vulnerability
World Bank GDP growth	World Bank Indicators API	Lagging/forecast where available	Annual	YoY %, revision	Higher = stronger
The World Bank Indicators API provides programmatic access to nearly 16,000 time-series indicators across more than 45 databases, and the IMF DataMapper API provides endpoints for retrieving time series and metadata used in DataMapper.  
________________________________________
6. Preferred Data Sources by Priority
Rank	Source	Best Use
1	FRED	U.S. macro, rates, yield curves, credit spreads, VIX, financial stress
2	World Bank Indicators API	Global and country-level annual macro indicators
3	IMF DataMapper / IMF SDMX API	WEO forecasts, global GDP, inflation, debt, fiscal balances
4	OECD API	Composite Leading Indicators, industrial production, confidence indicators
5	BIS Data Portal	Credit-to-GDP, debt service ratios, credit aggregates, global liquidity
6	Cboe / FRED	VIX and volatility data
7	Yahoo Finance via yfinance	ETF market proxies, asset-class momentum
8	CPB World Trade Monitor	Global trade volume, if accessible
9	National statistical agencies	Country-specific validation
________________________________________
7. Transformation Method
The model should convert all indicators into comparable standardized signals.
7.1 Frequency Alignment
Target frequency:
Monthly
Rules:
Original Frequency	Monthly Conversion
Daily	Monthly average for macro/rates; month-end for prices
Weekly	Monthly average
Monthly	Use as-is
Quarterly	Forward-fill within quarter or use nowcast interpolation
Annual	Use only for structural/slow-moving modules, not short-term timing
7.2 Basic Transformations
Use one or more of the following depending on indicator type:
Indicator Type	Transformation
Level indicators	Rolling z-score
Growth indicators	YoY %, 3M annualized, 6M annualized
Market prices	3M and 6M total return
Rates	Level, 3M change, 12M change
Spreads	Level z-score and change z-score
Survey diffusion indexes	Level minus neutral value, e.g., PMI − 50
Balance-sheet ratios	Level z-score, percentile rank
Forecasts	Forecast revision and level relative to history
7.3 Rolling Z-Score
For most indicators:
Zᵢ,t = (Xᵢ,t − mean(Xᵢ,t−240:t)) / std(Xᵢ,t−240:t)
Preferred window:
20 years = 240 monthly observations
Fallback windows:
Data Availability	Window
≥ 20 years	240 months
10–20 years	Full available window, minimum 120 months
5–10 years	Use percentile rank instead of z-score
< 5 years	Use as auxiliary signal only
7.4 Directional Normalization
All indicators must be transformed so:
Higher score = better growth / easier liquidity / healthier risk appetite
Examples:
Indicator	Raw Increase Means	Model Adjustment
Industrial production	Stronger growth	Keep sign
Unemployment	Weaker economy	Invert sign
Credit spreads	Higher stress	Invert sign
VIX	Higher stress	Invert sign
Yield curve slope	Easier/future growth	Keep sign
Real policy rate	Tighter policy	Invert sign
Inflation	More inflation pressure	Keep sign for Inflation Score, invert for overall cycle score
7.5 Winsorization
Before scoring:
Winsorize z-scores at ±3.0
This prevents extreme crisis readings from dominating the entire model.
7.6 Momentum Measures
For each indicator:
3M Momentum = X_t − X_t−3
6M Momentum = X_t − X_t−6
For price series:
3M Return = Price_t / Price_t−3 − 1
6M Return = Price_t / Price_t−6 − 1
For rates/spreads:
3M Change in bps = Rate_t − Rate_t−3
6M Change in bps = Rate_t − Rate_t−6
________________________________________
8. Scoring Logic
8.1 Indicator-Level Score
Convert each standardized indicator into a bounded score:
Indicator Score = clip(Zᵢ,t, −3, +3)
Then map to a 0–100 scale:
Scoreᵢ,t = 50 + (Zᵢ,t × 15)
Bounds:
Minimum = 5
Maximum = 95
Interpretation:
Score	Meaning
80–95	Very strong / very easy / very healthy
60–80	Positive
45–60	Neutral
30–45	Weak
5–30	Very weak / stressed
8.2 Category Score
For each category:
Category Score = weighted average of indicator scores
Example:
Growth Score =
0.30 × Industrial Production Score
+ 0.25 × PMI/CLI Score
+ 0.20 × GDP Momentum Score
+ 0.15 × Trade Score
+ 0.10 × Labor Momentum Score
8.3 Sub-Score Weights
Sub-score	Weight in Cycle Model
Growth Score	35%
Risk & Credit Score	25%
Policy & Liquidity Score	20%
Inflation Stress Score	20%, negative contribution
Overall:
Macro Cycle Score =
0.35G + 0.25RC + 0.20PL − 0.20IS
Where:
•	G = Growth Score
•	RC = Risk & Credit Score
•	PL = Policy & Liquidity Score
•	IS = Inflation Stress Score
To keep a 0–100 scale, use:
Adjusted Cycle Score =
0.35G + 0.25RC + 0.20PL + 0.20(100 − IS)
8.4 Inflation Stress Score
Inflation is not always “bad.” The model should distinguish between:
Inflation Condition	Interpretation
Low and stable	Positive
Rising from very low with rising growth	Reflationary
High and rising	Negative
Falling from high levels	Disinflationary relief
Falling because demand is collapsing	Recessionary
Suggested Inflation Stress Score:
Inflation Stress =
0.40 × Inflation Level Z
+ 0.35 × Inflation Momentum Z
+ 0.25 × Inflation Expectations Z
Then map to 0–100.
________________________________________
9. Regime Classification Rules
Use a two-axis regime model.
9.1 Core Axes
Growth Axis = Growth Score
Inflation Axis = Inflation Score
Thresholds:
Score Range	Signal
> 60	Strong / high
45–60	Neutral
< 45	Weak / low
9.2 Main Regime Matrix
Growth Score	Inflation Score	Regime
> 60	45–60	Goldilocks Expansion
> 60	> 60	Reflation / Late-Cycle Overheating
45–60	> 60	Late Cycle / Inflation Pressure
< 45	> 60	Stagflation
< 45	45–60	Slowdown
< 45	< 45	Contraction / Deflationary Bust
45–60	< 45	Disinflationary Slowdown
> 60	< 45	Early Recovery / Disinflationary Expansion
9.3 Credit and Liquidity Overlay
After classifying the macro regime, apply a stress overlay.
Risk & Credit Score	Overlay
> 65	Risk-on confirmation
50–65	Neutral confirmation
35–50	Fragile regime
< 35	Financial stress / crisis overlay
Example:
Growth > 60, Inflation 45–60, Risk & Credit < 35
= Expansion with financial stress warning
9.4 Policy Overlay
Policy & Liquidity Score	Interpretation
> 65	Easy liquidity
50–65	Neutral
35–50	Restrictive
< 35	Severely restrictive
Example:
Growth < 45, Inflation > 60, Policy & Liquidity < 40
= Stagflation with constrained central-bank response
________________________________________
10. Detailed Regime Definitions
10.1 Goldilocks Expansion
Conditions:
Growth > 60
Inflation 45–60 or falling
Risk & Credit > 55
Policy & Liquidity neutral/easy
Macro interpretation:
•	Growth is above trend.
•	Inflation is controlled.
•	Credit spreads are stable or tightening.
•	Volatility is low.
•	Central banks are not aggressively restrictive.
Portfolio interpretation:
Asset	Bias
Equities	Overweight
Cyclicals	Overweight
Credit	Overweight IG/HY
Duration	Neutral/underweight
Commodities	Neutral
Gold	Neutral/underweight
Cash	Underweight
________________________________________
10.2 Reflation
Conditions:
Growth rising
Inflation rising from low/moderate levels
Yield curve steepening
Credit spreads tightening
Commodities rising
Portfolio interpretation:
Asset	Bias
Equities	Overweight
EM equities	Overweight
Small caps/cyclicals	Overweight
Commodities	Overweight
Credit	Overweight HY selectively
Long-duration bonds	Underweight
TIPS / inflation-linked bonds	Overweight
USD	Underweight if global reflation is broad
________________________________________
10.3 Late Cycle / Overheating
Conditions:
Growth > 55 but decelerating
Inflation > 60
Policy tightening
Yield curve flattening/inverting
Credit still okay but deteriorating
Portfolio interpretation:
Asset	Bias
Equities	Neutral/selective
Quality equities	Overweight
Value/energy/materials	Tactical overweight
Long-duration bonds	Underweight initially
Credit	Reduce HY risk
Commodities	Overweight
Gold	Neutral/overweight
Cash	Begin increasing
________________________________________
10.4 Slowdown
Conditions:
Growth < 45
Inflation neutral or falling
Credit spreads widening
PMIs/CLI declining
Yield curve flat/inverted
Portfolio interpretation:
Asset	Bias
Equities	Underweight
Defensives	Overweight
Long-duration Treasuries	Overweight
Investment-grade bonds	Overweight
High yield	Underweight
Commodities	Underweight
Gold	Neutral/overweight
Cash	Overweight
________________________________________
10.5 Contraction / Recession
Conditions:
Growth < 35
Risk & Credit < 35
Labor market deteriorating
Financial stress elevated
Inflation usually falling, except stagflation cases
Portfolio interpretation:
Asset	Bias
Equities	Underweight
Credit	Underweight HY, prefer high-quality IG
Sovereign duration	Overweight
Cash	Overweight
Gold	Overweight/neutral depending on real rates
Commodities	Underweight
USD	Often overweight during global stress
________________________________________
10.6 Stagflation
Conditions:
Growth < 45
Inflation > 60
Policy constrained
Real income pressure
Credit deteriorating
Commodities elevated
Portfolio interpretation:
Asset	Bias
Broad equities	Underweight
Quality/value equities	Selective
Long-duration bonds	Underweight or cautious
TIPS/inflation-linked	Overweight
Commodities	Overweight
Energy/materials	Overweight
Gold	Overweight
Cash	Overweight
Credit	Underweight HY
________________________________________
10.7 Disinflationary Recovery
Conditions:
Growth rising from weak levels
Inflation falling
Policy easing expected
Yield curve steepening
Credit stabilizing
Portfolio interpretation:
Asset	Bias
Equities	Begin overweight
Long-duration bonds	Overweight early, then neutral
Credit	Add IG first, then HY
EM	Gradual overweight
Commodities	Neutral
Gold	Neutral/overweight if real rates falling
Cash	Reduce
________________________________________
11. Portfolio Interpretation Framework
The model should output a regime-based allocation dashboard, not automatic trades.
11.1 Asset-Class Mapping
Regime	Equities	Duration	Credit	Commodities	Gold	USD	Cash
Goldilocks	↑↑	→ / ↓	↑↑	→	→	↓	↓
Reflation	↑↑	↓	↑	↑↑	→	↓	↓
Late Cycle	→	↓ / →	↓	↑	↑	→	↑
Slowdown	↓	↑↑	↓	↓	↑	↑	↑
Contraction	↓↓	↑↑	↓↓	↓	↑	↑↑	↑↑
Stagflation	↓	↓	↓↓	↑↑	↑↑	→ / ↑	↑
Disinflationary Recovery	↑	↑	↑	→	↑	↓	↓
Legend:
↑↑ = strong overweight
↑ = overweight
→ = neutral
↓ = underweight
↓↓ = strong underweight
11.2 Fixed-Income Interpretation
Because this model is macro-cycle oriented, fixed income should be interpreted through:
1.	Duration exposure
2.	Credit exposure
3.	Curve exposure
4.	Inflation exposure
5.	Liquidity exposure
Your bond materials emphasize that bond returns come from coupon/principal payments, reinvestment income, and capital gains/losses from price changes. That is important for the portfolio framework because the same rate move affects short-horizon and long-horizon investors differently.  
Macro Signal	Fixed-Income Interpretation
Growth slowing + inflation falling	Add duration
Growth slowing + inflation rising	Avoid excessive nominal duration; prefer TIPS/short duration
Credit spreads widening	Reduce HY, prefer Treasuries/IG
Yield curve steepening after inversion	Early recovery signal
Policy easing expected	Duration and high-quality bonds benefit
Liquidity stress rising	Prefer sovereign bonds and cash
11.3 Equity Interpretation
Macro Signal	Equity Style Preference
Growth rising, inflation stable	Cyclicals, growth, small caps
Reflation	Value, energy, materials, industrials
Late cycle	Quality, low leverage, pricing power
Slowdown	Defensives: healthcare, staples, utilities
Stagflation	Real assets, energy, pricing-power companies
Recovery	High beta, EM, cyclicals
11.4 Currency Interpretation
Signal	Interpretation
Global growth rising + USD falling	EM and global risk assets supported
Global stress rising + USD rising	Risk-off
U.S. real rates rising	USD support, pressure on gold/EM
Fed easing + global recovery	USD weakening bias
11.5 Commodity Interpretation
Signal	Interpretation
Growth rising + inflation rising	Commodity-positive
Growth falling + inflation rising	Energy/supply-shock stagflation risk
Growth falling + inflation falling	Commodity-negative
USD falling	Commodity-supportive
China/global industrial cycle improving	Metals-supportive
 
12. Suggested Output Dashboard
Each monthly model run should produce:
12.1 Headline Output
Current Regime: Disinflationary Slowdown
Confidence: 72%
Macro Cycle Score: 46 / 100
Growth Score: 41 / 100
Inflation Score: 58 / 100
Policy & Liquidity Score: 44 / 100
Risk & Credit Score: 51 / 100
12.2 Signal Table
Category	Score	Direction	Interpretation
Growth	41	Falling	Weakening activity
Inflation	58	Falling	Still elevated but improving
Policy	44	Tight	Restrictive policy
Credit	51	Stable	Neutral stress
Liquidity	46	Weak	Conditions still tight
Markets	55	Improving	Risk appetite recovering
12.3 Portfolio Tilt
Asset Class	Suggested Tilt
Equities	Neutral/underweight
Long-duration bonds	Overweight
Investment-grade credit	Neutral/overweight
High-yield credit	Underweight
Commodities	Underweight
Gold	Neutral/overweight
Cash	Overweight
 
13. Known Limitations
13.1 Data Revisions
GDP, employment, inflation, and industrial production are revised after initial release. The model should store vintages when possible.
13.2 Publication Lags
Some of the best global indicators are annual or quarterly. They are useful for structural context but weak for short-term cycle timing.
13.3 U.S.-Centric Bias
FRED data is excellent, but overreliance on U.S. indicators can make the model too U.S.-centric. The global version should include GDP-weighted regional modules:
Global Score =
0.45 × U.S.
+ 0.20 × Euro Area
+ 0.20 × China
+ 0.15 × Rest of World
Weights can be adjusted using nominal GDP, PPP GDP, or market-cap exposure.
13.4 Market Signals Can Be Noisy
Equities, VIX, credit spreads, and commodities can move for technical reasons unrelated to macro fundamentals.
13.5 Inflation Regimes Are Nonlinear
Inflation falling from 8% to 5% is not the same as inflation falling from 2% to 0%. The model should consider both level and direction.
13.6 Credit Booms Can Look Positive Before They Break
Credit growth and easy financial conditions often score positively before crises. That is why the model should include vulnerability indicators such as credit-to-GDP gaps and debt service ratios.
13.7 Regimes Are Probabilistic
The model should not force a single regime if data is mixed. It should output probabilities:
Expansion: 20%
Slowdown: 45%
Stagflation: 15%
Recovery: 20%
13.8 Not a Standalone Investment Strategy
The model does not replace valuation, earnings analysis, risk management, position sizing, or investor-specific constraints.
 
14. Minimum Viable Model vs. Full Model
14.1 Minimum Viable Model
Use this first:
Category	Indicators
Growth	OECD CLI, U.S. industrial production, global PMI proxy
Inflation	CPI, core CPI, commodity YoY
Policy	Fed Funds, real policy rate, 10Y−2Y curve
Credit	HY OAS, IG OAS
Liquidity	Financial Stress Index, VIX
Markets	ACWI, SPY, EEM, HYG, TLT, GLD, DBC
14.2 Full Institutional Model
Add:
•	BIS credit-to-GDP gaps
•	BIS debt service ratios
•	IMF WEO forecast revisions
•	World Bank country-level indicators
•	Regional CLIs
•	Trade volume
•	FX reserves
•	Dollar liquidity indicators
•	Bank lending standards
•	Country-level inflation surprises
•	Market-implied inflation expectations
•	Cross-asset volatility
 
15. Recommended Final Model Formula
15.1 Sub-Scores
Growth Score =
0.25 × Real Activity
+ 0.25 × Leading Indicators
+ 0.20 × Labor Momentum
+ 0.15 × Trade
+ 0.15 × Market Growth Proxies
Inflation Score =
0.35 × CPI/Core CPI
+ 0.25 × PPI/Input Prices
+ 0.20 × Commodity Inflation
+ 0.20 × Inflation Expectations
Policy & Liquidity Score =
0.25 × Real Policy Rate Inverted
+ 0.20 × Yield Curve
+ 0.20 × Money Growth
+ 0.20 × Financial Conditions
+ 0.15 × Central Bank Direction
Risk & Credit Score =
0.30 × Credit Spreads Inverted
+ 0.25 × VIX/Volatility Inverted
+ 0.20 × Equity Momentum
+ 0.15 × EM Relative Performance
+ 0.10 × Funding Stress Inverted
15.2 Final Score
Final Macro Cycle Score =
0.35 × Growth Score
+ 0.25 × Risk & Credit Score
+ 0.20 × Policy & Liquidity Score
+ 0.20 × (100 − Inflation Stress Score)
15.3 Final Regime
If Growth > 60 and Inflation <= 60:
    Goldilocks / Expansion

If Growth > 60 and Inflation > 60:
    Reflation or Late Cycle

If Growth between 45 and 60 and Inflation > 60:
    Late Cycle / Inflation Pressure

If Growth < 45 and Inflation > 60:
    Stagflation

If Growth < 45 and Inflation between 45 and 60:
    Slowdown

If Growth < 45 and Inflation < 45:
    Contraction / Deflationary Bust

If Growth rising and Inflation falling:
    Disinflationary Recovery
Then adjust using:
If Risk & Credit Score < 35:
    Add "Financial Stress Overlay"

If Policy & Liquidity Score < 35:
    Add "Restrictive Policy Overlay"

If Credit-to-GDP Gap is extremely high:
    Add "Credit Vulnerability Overlay"
 
16. Best Practical Interpretation
The most useful version of the model is not a single score. It is a regime engine:
1. Identify growth direction.
2. Identify inflation direction.
3. Check policy/liquidity conditions.
4. Check credit and market stress.
5. Classify regime.
6. Translate regime into asset-class tilts.
7. Validate against valuation and risk constraints.
For your long-term portfolio work, the model should be used as a macro allocation compass:
•	It tells you when to be aggressive or defensive.
•	It tells you when inflation hedges matter.
•	It tells you when duration is attractive or dangerous.
•	It tells you when credit risk is being rewarded or mispriced.
•	It does not tell you the exact ticker to buy without further valuation and portfolio optimization.

