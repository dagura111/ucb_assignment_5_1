# assignment_5_1

**Data Visualization for Coupon Acceptance Prediction**
**Overview**
The goal of this project is to use visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data Source**
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 

**Project Goal**
The goal is to distinguish between customers who accepted a driving coupon and those who did not using visualizations and probability distributions.

**Data Exploration**
The dataset contains 12684 rows and 26 features.
Plotting, statistical summaries, and visualization revealed that
1. If you are alone or with friends and under the age of 21 and single most likely to use coupon
2. If you are with kids and weather is sunny, most likely to use coupon
3. If you are alone or and weather is sunny, most likely to use coupon
4. If you are driving to "no urgent place" then most likely to use coupon
5. High school and with 1 day of expiry will use the most coupon.
6. High school/no degree education want to use restaruant which is < 20
7. High school/no degree education want to use restaruant which is < 20

There are [unique categories] for [categorical feature], [range] for [numeric feature], etc.
**Data Preprocessing**
1. First I dropped the column car because it had 99% null values
2. Then I dropped Null rows because those are very handful and replacing them could impact the distribution.
3. Then I created the heat map to see the numerical relationship and didn't found any strong correlation
4. Then for categorial values I created individual bar plots to identify which ones have corelation with the coupon acceptance or not acceptance.
5. Then for categorial, I created violin plots to find out the co-relation of two categorial attributes with the coupon acceptance or not acceptance.

**Conclusion with one categorical variable**
1. Travelling with Friend(s) has the highest acceptance ration of 67.630241
2. Marital Status - Single has the highest acceptance ration of 61.028771
3. Income bracket 25000−37499, 50000−62499, and Less than $12500 has the acceptance ration of 59.718603, 58.977636 and 58.777120.
4. Weather sunny has the highest acceptance ration of 59.504218
5. Gender Male has the highest acceptance ration of 59.234694
6. Destination No Urgent Place has the highest acceptance ration of 63.400335
7. 2PM has the highest acceptance ration of 66.075157
8. 1D expiry has the highest acceptance ration of 62.781065
9. Occupations Healthcare Practitioners & Technical, Production Occupations, and Healthcare Support has the acceptance ration of 71.621622, 70.454545 and 69.834711
10. Bar coupons has accepted the most when the person has already visited 4~8 to the bar.
11. Coffee house coupons has accepted the most when the person has already visited 1~3 to the coffee house.
12. Carry away coupons has accepted the most when the person has already visited more than 8 times.
13. RestaurantLessThan20 and Restaurant20To50 coupons has accepted the most when the person has already visited more than 8 times.

**Conclusion with more than one categorical variable(s)**
1. If you are alone, single, 21 years of age and weather is sunny then most likely to use coupon
2. If you do not have a college degree then coupon expiry is within a day then most likely to use coupon
3. If your destination is no urgent place and you have visited the restaruant which is < 20 then most likely to use coupon.
4. If the weather is sunny and you have never been to coffee house then you are most likely to use the coffee house coupon.
5. If income is between 12,500 to 24,999 and never visited the coffee house then you are most likely to use the coffee house coupon.
6. If income is between 25,000 to 37,499 and visited the carry away 1 -2 times then you are most likely to use the coupon.
7. If income is between 25,000 to 37,499 and never visited the bar then you are most likely to use the bar coupon.
