# Tableau-Seattle-AirBnB-2016
Tableau Dashboard for AirBnB in Seattle for 2016

Link to the dashboard:
https://public.tableau.com/app/profile/daffa.firtiyan/viz/AirBnBSeattle2016Data_16733879086020/Dashboard1?publish=yes

Use case:
Someone trying to start an AirBnB business. What area should they buy a property and start renting it out. What other factors should they be looking at. Ultimately how much profit can they make.
Factors are:
- Location
- Bedrooms
- How much they can charge

Sheet1:
Where they would be able to charge the most by the region.

Sheet2:
A map visualisation of the same data as Sheet1

Sheet3:
If the person is thinking of listing it on AirBnB but also living in it. They want to know the best time to put it in the market to be able to use. When are people spending the most money on an AirBnB

Problem:
There is a massive drop on the week of 9 Jan 2017. This is due to the fact that the data for the date of 2 Jan 2017 is incomplete (not the full day). Fixed this by changing the filter to not include 2 Jan 2017.

Conclusion:
Not a lot of people use AirBnB from early Jan to late Feb, this could be because people don't really travel until the later part of the year. Just based on this graph, the most profitable time to rent out an AirBnB is during the American Summer and at the end of the year.

Sheet4:
Factors that would affect the price of an AirBnB. Looking at the amounts of bedroom.

Problem:
Bedrooms is a value dataset. Converted it to Dimensions.
Excluded Null and 0 bedroom AirBnB.

From SUM(Price) we can deduce that the most common number of AirBnB has 1 bedroom.
From AVG(Price) we can deduce that the most profitable number of bedrooms to have on an AirBnB is 6 bedrooms.

Conclusion:
There is a much higher ROI the more bedrooms an AirBnB has. For example, on average, you can charge 82.33% higher price on a 2 bedroom as opposed to a 1 bedroom AirBnB. On the extreme side, the average price of a 6 bedroom is 507.9% higher than a 1 bedroom AirBnB

Sheet5:
We would like to know what the person's competition look like in terms of the bedrooms.

Problems:
Needed to get a count for individual Id, because some (if not all) AirBnB listing's Id shows up more than once. Changed the the measure of Id as Count (Distinct)

Conclusion:
The more bedrooms you have, the less competition you have. There are 274.9% more 1 bedroom as opposed to a 2 bedroom AirBnB.

However, we would also need to figure out the demands. If the person bought a 4 bedroom house to list as an AirBnB but the demand for 4 bedroom AirBnB is low, then the purchase would be a terrible investment. 
Solution: we could look into the reviews to figure out the demand for a 4+ bedroom AirBnB


Other things to consider:
1. If the person wanted data for people who rent at least for a whole week or for a whole month
2. How many 5 star review people are giving on a 1 bedroom vs. 2 bedroom vs. 3 bedroom, etc.
