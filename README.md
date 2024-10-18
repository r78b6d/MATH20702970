java c
MATH2070/2970: Optimisation and Financial Mathematics
Semester 2, 2024
Data provided
The file project_data .csv is a comma-separated text file containing the stock prices from 1 July 2022 to 30 June 2024 (inclusive) for the largest 10 companies listed on the Australian Stock Exchange (ASX) by market capitalisation (i.e. total value of stocks):
• BHP — BHP Group Ltd, a mining company (mostly coal, copper, iron ore and oil)
•  CBA — Commonwealth Bank of Australia, aretail bank (manages savings, offers business loans, mortgages, credit cards, etc)
•  CSL — CSL Ltd, a biotechnology company (manufactures vaccines, antivenoms, etc)
• NAB — National Australia Bank, another retail bank
• WBC — Westpac Banking Corporation, another retail bank
• ANZ — ANZ Group Holdings Ltd, another retail bank
•  MQG — Macquarie Group Ltd, an investment bank (manages investments for other people and institutions, also offers some retail banking)
• WES — Wesfarmers Ltd, a big-box retail group (runs Officeworks, Bunnings, Kmart, ...)
•  GMG — Goodman Group, a commercial real-estate company (owns and manages warehouses, business parks, etc)
• FMG — Fortescue Metals Group, a mining company (primarily iron ore)
The stock prices are the end-of-day prices, adjusted to exclude the impact of corporate events (like payments of dividends) which affect the stated share price but do not reflect trading activity.
Questions1. For each of the 10 stocks, compute their simple returns  on day t. Calculate the mean and covariance matrix for the returns to 6 decimal places, and confirm they are

and

Use the above rounded values of r and C for the remainder of the project.
2. Find the optimal portfolio x(t) for investors with risk-aversion parameter t (i.e. your answer should be a function of t).
Which assets will never be short-sold by risk-averse investors?
3. Consider a specific investor with risk aversion parameter t = 0.06 who wants to invest $100,000 in these assets.
(a)  What is their optimal investment allocation, mean return and risk (standard deviation) of their investment?  Give all answers in $.
(b) (MATH2070 only:) Suppose now the investor does not want to short sell  any asset. Use SciPy minimize (with a tolerance tol  =  1e-15) to find their optimal portfolio, mean return and risk (standard deviation). Again, give all answers in $.Show that the portfolio obtained using SciPy is the optimal portfolio (possibly up to a small error) by verifying that it is a KKT point of the log-utility optimisation problem. Be aware: there will be a small numerical error that you must allow for in checking, e.g., that quantities equal zero, are non-negative, etc.
4. Illustrate this problem graphically: in the (σ,µ) p代 写MATH2070/2970: Optimisation and Financial Mathematics Semester 2, 2024R
代做程序编程语言lane, show (on the same graph):
(i)   The 10 assets
(ii)  The optimal (unconstrained) portfolio for the investor from Question 3(a)
(iii)  The minimum risk portfolio
(iv)  The efficient frontier and minimum variance frontier
You should format the plot with appropriate labels, etc.  I recommend using the axis ranges σ ∈ [0.005, 0.025] and µ ∈ [−0.0005, 0.002], but you may choose other values if you prefer.
5. Suppose now that the market also has a risk-free cash asset with return 0.00015 (which works out to around 3.8% annually, close to the current Australian bond rate).(a)  What is the new optimal portfolio for the investor from Question 3 (with short selling allowed)? Is this a borrowing or lending portfolio? (b)  In a new plot, show in the (σ,µ) plane:
(i)  The items from Question 4
(ii)  The optimal unconstrained portfolio for the investor with a risk-free asset  (Ques- tion 5a)
(iii)  The market portfolio
(iv)  The capital market line
I recommend you use axis range σ  ∈ [0, 0.025] for this plot, but you may choose other values if you prefer.
6. For this question, take the market portfolio to be the relative market capitalisations of the 10 stocks:
xM  = [0.191, 0.187, 0.116, 0.095, 0.088, 0.075, 0.072, 0.065, 0.06, 0.051].
(a)   Compute the betas of the 10 underlying stocks.
(b)  With reference to the underlying businesses, explain why the betas of CSL and MQG are so different. Your answer should be brief, at most 1 paragraph.
7. (MATH2970 only:)
(a)  Randomly generate 10000 feasible portfolios (according to what you think is a reasonable distribution) and plot them on the chart in Question 4.
(b)  Unless you have made a very informed choice of distribution, you will see that the portfolios do not fill up to the minimum variance frontier.  This is a result of the high dimensionality of the set of portfolios (10 stocks - 1 equality constraint = 9 degrees of freedom).
Generate 1 million feasible portfolios in the same fashion, and compute the (vector Eu- clidean) distance di  between each portfolio and the minimum risk portfolio.
On a log-log graph, plot P(di  < δ) against δ ∈ [0.1, 10], and show graphically that the rate of decay as δ → 0 is like a high-degree polynomial (theoretically, it should be δ−9).Use this, and the fact that the minimum risk portfolio is the unique global minimum for risk, to explain why there are very few randomly generated portfolios close to that of the minimum risk portfolio on the mean return–risk graph.
(c)  Randomly generate 10000 feasible portfolios that are close to the minimum risk portfolio, and plot them on the chart in Question 4. How well do they show the minimum variance frontier?





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
