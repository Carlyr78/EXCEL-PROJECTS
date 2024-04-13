
Customer Engagement Analysis in Excel Project

Case Description

In 2022, there were high expectations for the growth of the 365 company and increased student engagement based on the introduction of new website platform features. Some of these features included an XP system that enabled students to track their progress, level up, and earn rewards by completing various learning objectives. The platform also offered in-app coins that could be exchanged for special awards, a leaderboard where students could compete for top positions in different divisions, earning weekly rewards and advancing up the ladder, and streaks to motivate students to maintain consistent learning habits. Additionally, the company expanded its course library, covering a broader range of topics to provide its students with a richer set of skills and attract a larger audience. These enhancements were anticipated to positively impact the student experience, create an effective strategy for customer engagement, and contribute to the company's success in the coming year. With this Customer Engagement Analysis in Excel project, you must analyze whether the new additions to the platform have increased student engagement.

Task 1
In 2022, there were high expectations for the growth of the 365 company and increased student engagement based on the introduction of new website platform features. Some of these features included an XP system that enabled students to track their progress, level up, and earn rewards by completing various learning objectives. The platform also offered in-app coins that could be exchanged for special awards, a leaderboard where students could compete for top positions in different divisions, earning weekly rewards and advancing up the ladder, and streaks to motivate students to maintain consistent learning habits.

Please open the 'Engagement project.xlsx' file and navigate to the 'Task 1 and 2' sheet using Microsoft Excel. Your first task is to provide insights into the relative engagement levels in Q4 2021 and Q4 2022. You will focus on low-engagement users (those who watched between 1 and 100 minutes in 2021). Low-engagement users often represent the most significant potential for growth. If 365 can find ways to increase its usage, it could significantly impact the overall use of the platform.

If there are repeated students who watched in Q4 2021 and Q4 2022, how does their engagement compare between the two periods? Compute the mean, median, and standard deviation for these groups. Is there a difference in engagement between paid- and free-plan subscribers?

Open the 'Engagement project.xlsx' file and navigate to the 'Task 1 and 2' sheet using Microsoft Excel.
Apply the AVERAGE, MEDIAN, and STDEV.S Excel functions to the ‘minutes_watched’ column to compute the mean, median, and standard deviation for both groups (free- and paid-plan students).


3. Apply the AVERAGE, MEDIAN, and STDEV.S Excel functions to the ‘minutes_watched’ column to compute the mean, median, and standard deviation for both groups (free- and paid-plan students).

 
Task 2
Please open the 'Engagement project.xlsx' file and navigate to the 'Task 1 and 2' sheet using Microsoft Excel. Calculate the skewness and kurtosis of students who watched content in Q4 2021 and Q4 2022. Consider paid- and free-plan students. Does the result contradict the mean and median values previously obtained?

Task 3
Please open the 'Engagement project.xlsx' file and navigate to the 'Task 3 sheet using Microsoft Excel.

You will find information about two pairs of students:

Students who haven’t had a paid-plan subscription
Engaged in Q4 2021
Engaged in Q4 2022
Students who have been paid-plan subscribers
Engaged in Q4 2021
Engaged in Q4 2022
 For each of the four groups, determine the minute interval within which you can be 95% confident that a randomly selected individual will be situated.

What conclusions can you draw about the students’ engagement in Q4 2021 and Q4 2022?

Tip: Use the z-statistic when performing calculations.

Follow the general steps below to compute confidence intervals in Excel:

1. Determine your sample size (n)—the count of the number of observations in your data.

2. Calculate the sample’s mean value.

3. Determine the sample’s standard deviation.

4. Estimate the significance level.


5. Obtain the z-score from the standard normal distribution table for probability (p) = 1 - α/2. 


6. Calculate the standard error.


7. Calculate the margin of error.


8. Calculate the confidence interval by adding and subtracting the margin of error from the mean value.

Task 4
Use the data in Task 4 of the ‘Engagement project.xlsx’ to solve the following task.

You want to reach a data-driven customer engagement decision on whether the platform’s new features contribute to the increase of minutes watched on the platform for both free-plan and paying students—i.e., the rise in student engagement in their study process. To do that, use hypothesis testing on both groups (free-plan and paying) for 2021 and 2022.

Your null hypotheses should include the following:

The engagement (minutes watched) in Q4 2021 is higher than or equal to the one in Q4 2022 (μ1 ≥ μ2). We test free-plan and paying students separately.
Additionally, make the following assumptions:

For free-plan students, perform a two-sample t-test assuming unequal variances.
For paying students, conduct a two-sample t-test assuming unequal variances.
Optional: Perform a two-sample f-test for variances to support the assumptions.

What conclusion can you draw from this test? Comment on the results of committing a Type I or a Type II error in this study. Which one would result in higher costs for the company?


First, you must perform a two-sample f-test for variances to prove the assumption of unequal variances between the samples for free- and paid-plan subscribers. If you have the Data Analysis ToolPak installed in Excel, you can use it (as seen below) to perform the two-sample f-test for variances.

In the Data Analysis dialog box, select F-Test Two-Sample for Variances from the list of analysis tools and click OK.



In the F-Test Two-Sample for Variances dialog box, specify the Sample 1 and 2 ranges. You can enter the cell ranges manually or use the range selection tool to select the data in your worksheet.



Check the Labels box if your data has headers so Excel can treat them as labels.



Choose whether you want the output in a new worksheet or a specific location in your current worksheet. Click OK to run the analysis.

 

Excel will perform the f-test for variances and provide the test statistic (f-value) and the p-value. The p-value would indicate the probability of obtaining the observed f-value if the null hypothesis (equal variances) were true.

As mentioned, compare the p-value to your chosen significance level (alpha) to determine if the variances are significantly different. If the p-value is less than or equal to your alpha level, you can reject the null hypothesis of equal variances.

The next step is to perform a t-test and compare it to the critical value from the t-distribution.

Consider the following steps for paying students where the variances are assumed unequal.

1. Specify the significance level :

α
=
1
−
C
o
n
f
i
d
e
n
c
e
 
L
e
v
e
l
=
1
−
0.95
=
0.05
2. Calculate the t-statistic using the following formula:

T
=
(
¯
x
−
¯
y
)
−
μ
d
√
s
2
x
n
x
+
s
2
y
n
y
3. Look up the critical t-value using a t-distribution table (https://365datascience.com/calculators/tables/std-table/) to correspond to your chosen significance level (commonly 0.05) and calculated degrees of freedom. 

4. Note that the degree of freedom is calculated using the following formula for independent samples with unknown variances which are assumed to be unequal:

d
f
=
(
s
2
x
n
x
+
s
2
y
n
y
)
(
s
2
x
/
n
x
)
2
n
x
−
1
+
(
s
2
y
/
n
y
)
2
n
y
−
1
The degrees of freedom are assumed to be equal to 8,229.

Compare t-statistic to critical t-value. Interpret the magnitude and the sign of your t-statistic. The decision rule—based on the critical value approach—is as follows:

I
f
 
T
≤
−
t
d
f
,
0.05
 
,
 
r
e
j
e
c
t
 
H
0
I
f
 
T
>
−
t
d
f
,
0.05
 
,
 
f
a
i
l
 
t
o
 
r
e
j
e
c
t
 
H
0
Assume that the critical t-value equals 1.65.

The decision rule—based on the p-value approach—is as follows:

p
−
v
a
l
u
e
 
≤
 
α
 
,
 
R
e
j
e
c
t
 
H
0
p
−
v
a
l
u
e
 
>
 
α
 
,
 
F
a
i
l
 
 
t
o
 
r
e
j
e
c
t
 
H
0
Alternatively, you can use the Data Analysis ToolPak in Excel to obtain the result directly:

1. Click on Data Analysis in the Analysis group. Select ‘t-Test: Two-Sample Assuming Unequal Variances’ from the list of analysis tools and click OK.



2. In the ‘t-Test: Two-Sample Assuming Unequal Variances’ dialog box, specify for Sample 1 and 2 ranges.



3. Enter your desired significance level (alpha) in the Alpha field. Choose whether you want the output in a new worksheet or a specific location in your current worksheet.

Excel will perform the two-sample t-test assuming unequal variances and provide the results, including the t-statistic, degrees of freedom, and the p-value. The p-value would indicate the probability of obtaining the observed t-statistic if the null hypothesis (no difference between means) were true.

Compare the p-value to your chosen significance level (alpha) to determine if the difference between the means of the two samples is statistically significant. If the p-value is less than or equal to your alpha level, you can reject the null hypothesis of similar means.

Task 5
Your last task is determining whether the average number of minutes watched in the US is similar to that in India.

Understanding the differences in usage patterns can help in product localization. The platform might need to tailor its content, features, or user interface to better fit the preferences or needs of users in different regions.

You’ll focus only on free-plan students in 2022. Use the Excel sheet Task 5 to perform your calculations.

Your null hypotheses should (respectively) include the following:

The engagement (minutes watched) in the US is higher than or equal to that in India (μ1 ≥ μ2). We test only free-plan students.
The engagement (minutes watched) in the US is lower than that in India (μ1 < μ2). We test only free-plan students.
Additionally, perform a two-sample t-test assuming unequal variances.

Optional: Perform a two-sample f-test for variances to support the assumptions.

What conclusion can you draw from this test? Is the engagement in the US higher than that in India?


First, you must perform a two-sample f-test for variances to prove that assumption of unequal variances between the samples (minutes watched by free-plan subscribers in the US and India):


Excel will perform the f-test for variances and provide the test statistic (f-value) and the p-value. The p-value would indicate the probability of obtaining the observed f-value if the null hypothesis (equal variances) were true.

As mentioned, compare the p-value to your chosen significance level (alpha) to determine if the variances are significantly different. If the p-value is less than or equal to your alpha level, you can reject the null hypothesis of equal variances.

The next step is to perform a t-test and compare it to the critical value from the t-distribution.


1. Specify the significance level.


2. Calculate the t-statistic.

3. Look up the critical t-value using a t-distribution table (https://365datascience.com/calculators/tables/std-table/) to correspond to your chosen significance level (commonly 0.05) and calculated degrees of freedom.

4. Compare t-statistic to critical t-value. Interpret the magnitude and the sign of your t-statistic. 

Compare the p-value to your chosen significance level (alpha) to determine if the difference between the means of the two samples is statistically significant. If the p-value is less than or equal to your alpha level, you can reject the null hypothesis of similar means.
