# The Impact of Technical Wordings in Promotional Emails
In the fiercely competitive food delivery industry, effective advertising plays a pivotal role in maintaining market dominance. UberEats, a prominent player, seeks to optimize its promotional emails by understanding the impact of technical wordings, specifically acronyms and jargon, on subscribers' engagement. Contrary to conventional wisdom, which suggests simplicity in advertising, this study explores whether advanced language influences customers' inclination to click on promotional materials. 

Focused on active UberEats subscribers in New York City, the research employs a stratified sampling approach, randomizing participants into control and treatment groups. Statistical analyses, including chi-squared tests, will gauge the significance of technical wordings on click-through rates. The study aims to provide actionable insights for UberEats, with potential implications for the broader food delivery industry. [PowerPoint](https://drive.google.com/file/d/14yaDmSQAuAhhE40wJeSADLfIDFuXGyPp/view)

## Research Plan

![alt text](https://github.com/imkir0513/technical_wordings_in_promotions/blob/master/images/research%20plan_1.png)

In this study, our specific focus is on the technical language used in promotional emails. To provide a more measurable and actionable recommendation for UberEats, we have narrowed our research to examine the proportion of jargon and acronyms. We hypothesize that promotional emails containing more than three technical terms in a 95-100 word advertisement will have a more effective impact than those without any technical language. Subscribers will be randomly assigned to one of three email types: those without any technical language, those with more than three jargon words, and those with more than three acronym words. Finally, we will use the chi-square test to determine which group of recipients uses the coupon in the email most frequently.



## Hypothesis

![alt text](https://github.com/imkir0513/technical_wordings_in_promotions/blob/master/images/hypothesis.png)

We have chosen a confidence level of 95% for rejecting the null hypothesis (H0). Regarding the first research question, if the p-value is less than 0.05, we reject H0, indicating a statistically significant difference in customers' inclination to view promotional emails with varying levels of technical language. Similarly, for the second research question, if the p-value is less than 0.05, we reject H0, signifying a statistically significant difference in customers' inclination to view promotional emails with different levels of acronyms.

## Sample Selection

![alt text]([https://github.com/imkir0513/technical_wordings_in_promotions/blob/master/images/research%20plan_2.png))

For sample selection, we employed stratified sampling to ensure a representative sample that captures the diversity of our target population. Stratification was based on customers' past yearly expenditures on Uber Eats. We aimed to gauge sensitivity to specific elements within each stratum by organizing customers into five spending categories in the last 6 months: $50 and less, $51-$100, $101-$150, $151-$200, and $201 and more. This approach aligns with best practices, considering both the recommendation of using no more than 4-6 stratification variables and 6 strata in a sample, as well as accounting for recently signed-up users with no previous order history.

## Statistical Plan 

![alt text]([https://github.com/imkir0513/technical_wordings_in_promotions/blob/master/images/statistical_plans.png))

We analyze data from different groups, focusing on whether acronyms and jargon impact coupon usage. Using the Chi-square test in R, we compare groups with and without technical terms. The test checks if proportions of coupon users differ.

For example, in assessing acronyms, we count coupon users in the control and treatment groups. The 'chisq.test' function in R helps with this:

(chisq.test(bp.dat$data.Group, bp.dat$data.coupon, correct = TRUE))

The results show 'Yes' proportions and p-values. If proportions differ and the p-value is below a chosen level (usually 0.05), we reject the idea that the impact of technical terms is the same in both groups.

## Limitations and Uncertainties

A key limitation of this study is the potential for selection bias. Our sample is exclusively drawn from UberEATS subscribers, limiting the generalizability of our findings to a broader population. For instance, if UberEATS subscribers differ significantly from the general population of food delivery service users, our conclusions may not apply universally. This is particularly relevant if UberEATS subscribers have a higher income than users of other services like Chowbus.

Additionally, the study faces uncertainty regarding potential hidden traits among UberEATS subscribers. As mentioned earlier, we measure customer preference based on coupon usage, but this might not capture the full picture. Factors like email delivery issues or customers not reading the promotion could affect results. While we can compare the impact of different promotional designs, we cannot definitively attribute non-order placement solely to a lack of responsiveness to the promotion. This limitation prevents us from accurately assessing the effectiveness of the designs and computing conversion rates.
