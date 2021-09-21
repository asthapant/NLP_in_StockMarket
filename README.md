# NLP in Stock Market

#                                                         Lazy Prices
##                              LAUREN COHEN, CHRISTOPHER MALLOY, and QUOC NGUYEN

# Introduction:
The paper ‘Lazy Prices’, makes use of the firm's annual financial reports- 10K and examines that the extent of changes in these documents impact the stock prices significantly. The paper asserts that there has been a lack of announcement return associated with these changes, and that is not due to these corporate documents becoming less informative or less useful. The results analyse that 10Ks contain rich information but investors are missing a large part of information, perhaps due to increased complexity and length, resulting in zero announcement effects associated with these changes.
Using bar plots, we find that the length and textual changes of annual 10Ks have increased substantially from the year 1995 to 2017. 
The authors then present an example of Baxter International Inc., a bioscience and medical products firm. Around 2 months after the release of Baxter’s 10K reports, a New York Times article published that the US Food and Drug Administration(FDA) was imposing tighter regulations on procuring automated pumps. The news further stated that FDA imposed a large recall on Baxter, following which its stock returns fell substantially. In contrast, there was no reaction to Baxter’s own 10K reports, released well before the news reports. However, there is evidence that its 10K for the year were considerably changed relative to last year, with the introduction of more terms signaling the impending downfall.
This leads to the suggestive conclusion that the firms that change their reports experience significantly lower future stock returns.

# Workflow:
The study covers the entire universe of publicly traded firms, since all of them are mandated to file 10Ks annually. The long ‘non changers’ and ‘short changers’ experience an increase in value weighted abnormal returns which accrue up in the following months. This shows that the effect of these filings gets incorporated into asset prices gradually in a few months. 
Then, the authors explore the mechanism behind these return results. They show that although the MD&A section in the reports has more discretion and flexibility in terms of content, and it does predict abnormal returns, the changes in the Risk Factors section are more informative for stocks. The changes in language referring to the executive team, litigation or lawsuits and the extent of sentiment also affect the future returns.
The changes to these reports also predicts the future earnings, profitability, bankruptcies and future news announcements. But all these future prospects appear to be largely unanticipated.
The negative relationship between these changes and future returns is well explained by two major reasons:
The use of Natural Language Processing on it, retrieves 86% of changes consisting of negative sentiment changes, in comparison to the 14% positives which predict positive returns.
Second, there have been claims of omission of negative news to existing shareholders, thus increasing the risk of failing to report negative information, leading to asymmetric realisation of observed changes.

The effects documented are not driven by any factors such as firm size, industry, time, firm events, length or length changes of the documents. The paper highlights the ‘laziness’ of the investors towards a financial text compared to similar numerical reports. However, the comparison of last year’s textual reports to this years, gives out crucial information for the firm’s future operations. To examine the investor's attention, the data is used from the Securities and Exchange Commission (SEC) to receive every downloaded file, timestamp of download and IP address of downloader. From this, a panel data of the 10K downloading activity is made. Then it identifies the 10K releases for which a number of investors download the current and previous year’s data. When more investors compare and pay attention to the changes, the documented results are thereby attenuated indicating that inattention is the mechanism behind the findings.

# Literature Review:
The paper documents three main aspects:
The impact of investor inattention in stock prices
The use of textual analysis in finance and accounting
The information content of the firm's disclosure choices.

The data is procured from the SEC log files to show that the variation in attention to these annual reports leads to variation in return predictability patterns. It is not merely the difference in quantitative and qualitative information that matters for investors, but also the way in which qualitative information is constructed and presented(say with the use of more comparative statements). When it comes to textual analysis, it claims that the annual reports of firms with lower earnings are harder to interpret. Also the firms that are subject to litigation risk change their cautionary language to a larger degree relative to the previous report.

# Data and Summary Statistics:
The complete reports of 10-K, 10-K405, 10-KSB, and 10-Q filings are downloaded from the SEC’s EDGAR website from 1995 to 2014. Thereby, only the textual content of these reports is extracted and all other entities with numerical content greater than 15% are removed. 
Then four similarity measures are deployed to capture quarter on quarter similarities between 10K and 10Q findings. These include:
Cosine Similarity: For the set of terms in two documents, we first consider its union and compute separate frequency vectors containing the number of occurrences of each term of the union in the respective documents. Then, the dot product of these vectors divided by the respective norms gives cosine similarity.
Jaccard similarity: This uses the same frequency vectors and computes the norms of its intersection over the norm of its union.
Minimum edit distance: This is computed by counting the smallest number of operations required to transform one document into the other.
Simple similarity: This is a simple side by side comparison method. While comparing with the old document, we count the number of words in those changes, additions, and deletions and normalize the total count by the average size of the old and new document.
We then list the schedules of both the annual 10K reports(15 schedules) and quarterly 10Q reports(10 schedules). Thereby, we plot summary statistics for the final dataset for a period of around 20 years. In the Panel A, the properties like count, mean and standard deviation are labelled for characteristics such as Document Size, Sentiment, Uncertainty, Litigiousness of change, Change CEO and Change CFO. 
The panel represents these properties for the four similarity measures and Panel C reports the correlations between these measures. 

The Implications of change in Reporting Behaviour:

# A. Calendar-Time Portfolio Returns
The approach targets to analyse the future stock returns of the firms who change their yearly reports in comparison with those who don’t. The author divides the firms in namely 5 Quintiles from Q1 to Q5, with Q1 encapsulating the firms that have the least similarity (big changers) and Q5 corresponding to firms with most similarity (little to no changers) in their reports this year and last year. The portfolio is rebalanced monthly. The reports are collected corresponding to 4 quarters of the year (for 3 quarters, we deploy the 10Q reports and for the quarter involving the fiscal month end, we use the 10K reports) and similarity is measured relative to last year’s report. The stock in the portfolio is both equally and value weighted (depending on the market capitalization) and the corresponding results are analysed.

# Returns Accessed: 
- Excess returns : To quantify how much the funds have performed relative to the benchmark. As described under the CAPM, excess returns are formulated as: 
Risk free rate+Beta of security* (Expected return of the market-Risk free rate)- Actual Return
- Fama French Three Factor Model: Quantifies the excess returns based on three different parameters; Market Risk, Outperformance of companies with high book to market ratio, Outperformance of large cap companies.
- Fama French Five Factor Model: Incorporates the additional two parameters of profitability and investment.

# Observations:
The return values of L/S portfolio (Q5-Q1) are significant and do not depend on risk factors/market parameters. The results remain invariant for all four similarity measures. For the value weighted portfolio returns, the L/S return values are high in comparison to equally weighted and differ as per similarity technique used.
The authors then plot the cumulative abnormal returns(CAR) for each quintile with time of six months following the portfolio formation and the following observations are recorded.
Panel A:
For the little to no changers(Q5), the CAR quickly drops to zero, while for Q1, it descends to more negative values in the next six months.
Panel B:
This chart evaluates the returns with scrutiny over the ten days before and after the filing. However, no economically detectable change is found around the period.
Following this, it is concluded that the decision to change the reports to a fair extent does affect the firm’s future returns, but are more pronounced over some months, and not shortly after the release.

# Characteristics Of Quintile Portfolios:
The authors curate a table depicting the Market value of Equity, Shorting cost, Monthly Turnover and Sentiment of Change for all the five quintiles and observe that the firms falling under Q1 are slightly larger with low shorting costs, thus ensuring that the sample space covers all kinds of publicly traded firms, be it small or big, given that the 10Ks and 10Qs are mandated for each of them.

# Fama Macbeth Regression:
The two step regression determines how the market factors describe the asset pricings.
Step 1: The expected returns are regressed against the time series of the factors to predict values of factor exposure/coefficient(beta)
Step 2: For each time step, the asset returns are regressed against the estimated betas to determine the time series of risk premium(lambda) for each factor.
These coefficients are then averaged out for each factor. The risk premium defines how the risk coefficient affects the stock return.
P Value and T Score: 
P-Value is defined as the probability that any observable difference occurred by a random chance. Thus, the lower the p-value, less are the chances of any random effect.  
T-Statistics are computed for each risk premium and are defined by the standard deviation of the risk premiums and the total time period.

The authors run the FamaMacbeth regression model over a set of additional market predictors. 
Size: The log market value of Equity/market capitalisation. (current stock price*outstanding shares)
log(BM): The log of the book value of the equity over the market value.
Standard Unexpected Earnings(SUE): The difference between the reported earnings and the expected earnings for a particular firm.
Ret(−1,0) indicates the firm’s previous month’s return
Ret(−12,−2) indicates the cumulative stock return from month t − 12 to month t − 2.

The result table indicates the factor coefficient, t stats(in brackets) and p values(depicted by asterisks for levels 1%, 5% and 10%); for the four different similarity measures.

# Mechanism:

A. Explaining Changes in Reporting Behavior
To better understand what factors affect the similarity scores, the authors panel regress the similarity measures (Simple Similarity) on the characteristics describing the document.
The characteristics are namely:
Sentiment of change: The number of negative words present normalized by the size of the change.
Uncertainty of Change: The number of words categorized by uncertainty normalized by the size of the change.
Litigiousness of Change: Similar approach for words categorized by litigiousness.
Change CEO and Change CFO: Binary feature which is 1 and 0 if there is a turnover in CEO or CFO respectively.

The results show that less similarity (i.e. more changes) across documents is associated with more (negative) sentiment, higher uncertainty, more litigiousness, and more frequent mentions of CEO and CFO changes.
Now, we regress the returns by FamaMacbeth approach while controlling these document level characteristics. Some specific characteristics like Positive Sentiment of change are also used to to separate out the sentiments, defined as number of positive words in Change, normalized by the size of Change.
From what is observed, there are effects of changes like decreasing sentiment or increasing the length of filing, but they aren't as strong as the impact of similarity measures in predicting the stock return. 

B. Isolating Key Sections of Report
The authors plot two bar graphs to show the average similarity score(Jaccard Similarity) of each section of 10K(Panel A) and 10Q(Panel B) reports. It is observed that the MD&A section in both the panels displays significantly lower average similarity than the other categories. 

C. Return Predictability of Key Sections of Reports
Now, we follow a similar approach as before and examine the return predictability associated with the similarity in each section of the report (earlier we analysed it for the entire report).
We first compute the similarities(all fours) for each textual section of the report relative to the last year’s report, and thus divide the firms in 5 quintiles. Thereby, we procure the top minus bottom(Q5-Q1) calendar time portfolio returns for both equal and value weighting of the stocks. 
Observations: We find that maximum effects on the returns is associated with the changes in the Risk Factor Section(upto 188 basis points every month).
Thus, a bar graph is plotted depicting the same for each similarity measure and see the high predictability of the risk factor section. These results hence prove that subtle and undetectable changes in some sections of the reports might have huge implications in the firm's future returns.

D.  Interacting with Investor Attention:
The authors make use of the SEC EDGAR database which contains the records of all downloads of corporate filings, mathed to the IP address of downloader. They then run Fama-Macbeth regression of firm level stock returns on similarity measure and other variables such as IPAccessMultipleYear(unique IP addresses accessing both current and previous year’s reports for a firm normalised by total number of unique IP addresses accessing current year’s).
We observe that when investor attention to these filings is greater, the return predictability results documented in this paper are weaker.
To analyse investor inattention in detail, it is seen how markets fail to incorporate changes in qualitative as opposed to quantitative information. We isolate the firms that make comparative statements(roughly one-third) in their annual or quarterly reports from those who don’t. This comparative sample is subdivided into those that make explicit textual comparison to specific accounting variables. Then, we divide these two sets of firms into five quintiles based on similarity and report the calendar time portfolio value weighted five factor alphas for both.
Conclusion:
The primary return predictability results are driven by the firms who do not make explicit textual comparisons to prior filings. The firms that draw attention to previous years are less likely to have changes go unnoticed by markets. The firms with investors conducting multi year downloads from SEC servers, have greater short run announcement effect with weaker long term return predictability results. 

E. Real Effects:
Now, we look at the extent to which the changes in document similarity predicts a firm’s future operating performance. The regressions of operating income, net income and sales are performed on the similarity score. These accounting variables are measured two quarters ahead and winsorized at 1% level. We observe that all four similarity measures significantly predict these three measures of operating performance.

F. Other Sorts and Tests of the Mechanism
The authors then run additional tests and tabulate the results. The return results are higher for documents with low sentiment, high litigiousness and high uncertainty (high and low defines wrt the median). Also, decrease in similarity also predicts increase in number of future 8 Ks, increase in future short interest, negative future earnings surprises, and increases in the number of future bankruptcies(forecast bad news for firms). We then run a regression of Jaccard similarity measures on depreciation rate, sales growth, capital expenditure and age. From what is observed, depreciation rate and firm age are negatively related while sales growth and expenditure are positively related to similarity score, indicating that firms modify their reports as they mature. 

G. Additional Robustness Checks
To perform robustness checks, the authors rerun the FamaMacbeth regression with additional characteristics: accruals, investment, gross profitability and free cash flow. As per observation, none of these variables drive the return predictability. Next, after sorting each industry into quintiles, they run an industry adjusted version of the calendar time portfolio, to test if the results are concentrated in any particular industry and the results remain strong and significant after making the industry adjustment. Finally, they confirm that the results are not affected by including stop words or by filtering of the SEC filings.
