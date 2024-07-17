ANALYSIS PERFORMED BY:
	Adrian Grzybowski


LINK TO ANALYSIS:
	https://github.com/AdrianGrzybowski/Coupon_ML_exercise/blob/main/prompt.ipynb


OBJECTIVES:
	Identify factors influencing drivers decisions for accepting coupons. 


DATA SOURCE:

	UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. 
	The survey asks the driver whether he will accept the coupon if he is the driver based on attributes described below:
	
	Coupons categories: 
	1.	Bar
	2.	Coffee houses
	3.	Carry out & take away
	4.	Less expensive restaurants (under $20)
	5.	More expensive restaurants ($20 - $50)
	
	The attributes of this data set include:
	1.	Gender: male, female
	2.	Age: below 21, 21 to 25, 26 to 30, etc.
	3.	Marital Status: single, married partner, unmarried partner, or widowed
	4.	Number of children: 0, 1, or more than 1
	5.	Education: high school, bachelors degree, associates degree, or graduate degree
	6.	Occupation: architecture & engineering, business & financial, etc.
	7.	Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
	8.	Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
	9.	Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
	10.	Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
	11.	Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
	12.	Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
	13.	Driving destination: home, work, or no urgent destination
	14.	Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
	15.	Weather: sunny, rainy, or snowy
	16.	Temperature: 30F, 55F, or 80F
	17.	Time: 10AM, 2PM, or 6PM
	18.	Passenger: alone, partner, kid(s), or friend(s)
	19.	time before it expires: 2 hours or one day
	20.	Coupon acceptance: Yes/No


FINDINGS FOR BAR COUPONS:

	1. Going to a bar more than one time a month is strongly correlated with a bar coupon acceptance
	2. Not driving with kid(s) is positively correlated with a bar coupon acceptance
	3. Being under 30 years old is positively correlated with a bar coupon acceptance
	4. Lower income for drivers that go more than 4 times a month to a cheap restaurant positively correlated with a bar coupon acceptance
	5. Whether working for farming, fishing, or forestry has any effect on accepting bar coupons is obscured by insufficient data
	6. Whether being widowed has any effect on accepting bar coupons is obscured by insufficient data


NEXT STEPS AND RECOMMENDATIONS FOR BAR COUPONS:

	1. It is possible that going out to eat/drink more often might be correlated with a bar coupon acceptance, I recommend testing for correlations with drivers
	that go to coffee shops more often as well as more expensive restaurants category.
	2. It is possible that individuals that make less money as well as some low income occupations might be correlated with coupon acceptance, I recommend testing
	for correlation among those groups.


FINDINGS FOR COFFEE HOUSE COUPONS:

	1. 49.63% of drivers accepted Coffee House coupon.
	2. Frequency of going to Coffee House is strongly correlated with acceptance of Coffee house coupons (Never : 17.5%, less than 1 : 48.1%, 1-3 : 64.8%, 4-8 : 68.2%, more than 8 timesin a month : 65.8%).
	3. Frequency of going to more expensive restaurants is correlated with acceptance of Coffee house coupons, with less frequent vistits negatively corrrelatingwith acceptance of the coupon, and more frequent visit positively correlated (Never : 42.6, less than 1 : 49.8%, 1-3 : 51.6%, 4-8 : 56.8%, more than 8 times in a month : 63.7%).
	4. Late morning (10AM : 63.5%) and early afternoon (2PM : 54.5%) positively correlated with acceptance of the Coffee House coupon, while late afternoon (6PM : 41.2%),night (42.9%) and early morning (44.0%) are negatively correlated with acceptance of the coupon.
	5. Drivers below age of 21 are more likely (67.8%, N=143) to accept Coffee house coupon, while drivers above 50 are less lieky (42.0%, N=529) to accept the coupon.
	6. Drivers are more likely to accept Coffee House coupon when they are not going Home (36.3%) or Work (44%) vs No urgent place (57.8%).
	7. Longer driving time to destination is negatively correlated with acceptance of the Coffee House coupon (GEQ15min : 45.1%, GEQ25min : 34.2%)
	8. Most categories of occupation have insufficient data for confident calling correlation with acceptance of Coffee House coupon. However some occupations have moreobservations - Sales & Related (40%, N=348), Retired (40%, N=161), Education&Training&Library (41%, N=273), Office & Administrative Support(43.8%, N=192), Management (45.4%, N=271), Student(61.5%, N=475).
	9. Driving with a Friend(s) (59.7%) or a Partner (56.7%) increased Coffee House coupon acceptance vs driving with Kid(s) (47.2%) or alone (43.4%) which decreased likelyhood of accepting the coupon.
	10. Drivers prefer longer expiration (1 day : 58.1%) over short expiration (2hr : 42.9%) for accepting Coffee House coupon.
	11. Frequency of going to cheaper restaurants is correlated with acceptance of Coffee house coupons, with less frequent vistits negativelycorrrelating with acceptance of the coupon(Never : 40.0%, less than 1 : 45.0%, 1-3 : 49.8%, 4-8 : 51.4%, more than 8 times in a month : 52.4%).
	12. Perhaps buying takeaway food less than 1 time a month is negatively correlated with accepting Coffee House coupon (43.4%, N=552). Category 'never' have weak statistical power (48.5%, N=33).
	13. Snowy weather (42.8%, N=285) discouraged drivers from accepting Coffee House coupon, while Sunny (50.1%, N=3316) or Rainy (51.6%, N=215) is likely neutral for accepting the coupon.
	14. achelor degree (45.6%, N=1276) is perhaps negatively correlated with acceptance of Coffee House coupon while House School graduate (54.0%, N=272) is perhaps slightly positively correlated. 'Some High School' category (60.7%, N=28) have too few observations to be confident
	15. Warmer air temperature (80F : 52.7%, N=2298) weakly correlates with acceptance of Coffee House coupon while cooler temperatures (30F : 44.1% N=299; 50F : 45.2%, N=1219) are negatively correlated with acceptance of the coupon. 
	16. Effects of martial status on acceptance of Coffee House coupon are hard to call due to small magnitude of changes between categories (Widowed : 35.3%, N=34; unmarried partner : 47%, N=676; married partner : 49.1, N=1466; Single : 51.4%, N=1497, Divorced : 51.7%, N=143). Category widowed does not have sufficient number of observations (N=34) to be confident about the effect size.
	17. There is weak correlation with same direction of travel being slightly preffered (52.7%, N=716) for acceptance of the Coffe coupon, vs the opposite direction (49.6%, N=3100).
	18. Having children is likely to neutral or have small effect on acceptance of Coffee House coupon (No children : 50.2% N=2360; Children : 48.8%, N=1456).
	19. Gender is neutral or a has weak effect on acceptance of the Coffee House coupon (Female : 49.1%, N=1969; Male : 50.2%, N=1847)
	20. There is no clear trend in frequency of going to bar and acceptance of Coffee House coupon.
	21. There is no clear trend in income and acceptance of Coffee House coupon.


NEXT STEPS AND RECOMMENDATIONS:

	1. Perform bivariate analysis based on the results of univariate analysis of factors influencing driver's acceptance of Coffee House coupons.
	2. Perform analysis of other coupons to uncover other relationships: Restaurant(<20) coupons, Restaurant(20-50) coupons, Carry out & Take away coupons.
