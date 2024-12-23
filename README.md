# R-Project

# Dataset

The NLSY97 dataset is the, a study tracking various life outcomes, including income, education, and family background, conducted by the Bureau of Labor Statistics (BLS).

The analysis focuses on identifying gender(i.e., male, female) differences in income/assets, exploring how these differences vary based on other factors such as employment (i.e., wages, hours, jobs, employment benefits), education (i.e., Career instruction, academic achievement, and attending school.), family background (i.e., socioeconomic status, family structure, the role of parents), race, marital status (i.e., never married, marriage, separation, divorce), and childhood household net worth, criminal history.

It is basically to make information available for labor demand activities in the market to collect information on American youths’ workforce actions along with additional crucial moments. The main idea is to follow an accurate representation that included men and women aged 12 to 16 on December 31 of 1996, while they moved from education through the workforce to growing up. Dataset size: Approximately 9000 individuals. (to be the exact 8,984 respondents)

Survey timeline: Initial question interview in 1997; following 1997, further inquiries were carried out either yearly or every two years, to notice changes, and long-term results.

Data usage: Policy making, Research and scheme evaluation.

# Model-3 Analysis

In statistics, Welch's t-test, or unequal variances t-test, is a two-sample location test which is used to test the (null) hypothesis that two populations have equal means. It is named for its creator, Bernard Lewis Welch, and is an adaptation of Student's t-test,[1] and is more reliable when the two samples have unequal variances and possibly unequal sample sizes.here, unequal variance, different sample size between male and female and more reliable than student's t-test. It will show the 95% confidence interval. Sample size is df here is 8842.1, substantial larger size for both male and female groups. The CLT theorem ensures, that sampling distribution of the mean is normal here. When you've got a big sample size, a Welch t-test continues to produce precise outcomes regardless of whether the information from the research isn't quite regularly distribution. here male and female group data assumed to be normally distributed as stated in the question. matters when sample size is less than 30. Same for the sampling distribution of the difference in means, as here. But, we are getting df=8842, so its presumed normal according to CLT. And, Welch's t-test is good for it. So, it's a good thing to get result.

# Conclusions and Discussion:
Key Insights: 
1. Gender Pay Gap: Significant income disparities persist between males and females, even after controlling for education and other socioeconomic factors. Higher education, and childhood household economic factors plays significant role for the future income.
2. Education and Income: Education is a critical driver of income, but its benefits are not enough to close the gender gap.
3. Intersectionality: Income disparities are influenced by both gender and race, emphasizing the need for multifaceted policy interventions.
4. We got the best distribution and results under Model-3 (Model-3) Variables with meaningless above 80% excluded and moderate-missingness variables imputed using mean for dependent variable and imputation for continuous variable and different ‘NA’ category for missing variables, compared to model-1 (including null values) and Model-2 (omitting of all null values).
5. So, for all, Model-1 (no NA removal), Model-2 (Omit observations with all missing value/-s in a row, even when the single missing values in the row), and Model-3(Variables with meaningless above 80% excluded and moderate-missingness variables imputed using mean for dependent variable and imputation for continuous variable and different ‘NA’ category for missing variables), we can confirm by looking at p-value and 95% confidence interval, males earning substantially more on average than females. P-value is here higher in non-top-coded model than top-coded model, to reject the null hypothesis.
6. For male group, highest degree (more significant), childhood household net worth, race plays a significant role for income. Same for the Model-1 and Model-3. For female group, dad-mom’s highest-grade completed, highest degree (more significant), childhood household net worth, plays a significant role. Overall, a highest degree (more significant), childhood household net worth are more important for both gender group and more significant to the income outcome.
7. Yes, from dependent variable and independetvariable, our Model is fit. But having the correct data instead of missing values, would be a great. Right now, we do only have result from impute() method for continues independent predictors.

# Limitations:
1. Low F-value in regression: The regression model has lower F-value. Although it gets p-value comparatively low.
2. Expecting some more negative co-efficients in Regression model-2.
3. Missing Data: Imputation may have introduced biases, particularly in highly missing variables. But having the correct data instead of missing values, would be a great. Right now, we do only have result from impute() method for continues independent predictors. Like occupation/industrial job, last 30 days drug history and etc. many respondents have skipped answers.

# Confidence in Findings:
The results are robust for academic discussions but would benefit from further validation before informing policy decisions. Missing data is the real problem. Although, i believe mentioned independent predictors above can make a difference as I tested, all Top-coded and Non-Top-coded with Models-1,2 and 3, almost all is getting T-test hypothesis result and regression result correct. So, I believe in taking this tests. Given the result for confidence interval, a hypothesis test and a regression model, I am confident enough in your analysis and findings to present them to policy makers.
