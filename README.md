# gini-coefficient
A short Mathematica file deriving the Gini Coefficient for a normal income distribution. This .nb file isn't properly viewable in github and will require a copy of Wolfram Mathematica to look at.

The notebook begins with a definition of the Gaussian normal[x], which gives a normal distribution of incomes for a population with average income mu and standard deviation sigma, with a plot of normal[x] to verify Gaussian shape. This equation specifies the percentage of the population with a certain income, so the average income, mu, will be the most common income. In this example, the average income is set to 50 and the standard deviation is 10.

A second equation translates normal[x] from a percentage graph to pop[x], the number of people with an income x. It also rounds the population to ensure that each population measure has an integer value. The scale has been set so that 1 person has an income of 20 dollars. pop[x] is then plugged into a table assessing the number of people with income x from 0 to 100.

This table is used to create a cumulative income distribution function by summing a product of each income x with the amount of people with x income, pop[x], and plotted onto another graph. This is strikingly similar to an integral of the normal distribution, the sigmoid error function. 

The data is then interpolated into a new funtion and integrated once to give the Lorenz curve. This curve describes what percent of all income the poorest x% of the population owns. The further the Lorenz curve deviates from a straight, diagonal line from (0,0) to (1,1), the more inequality exists in a population. The Lorenz curve is integrated one more time to give the value of the area under the curve. This area under the Lorenz curve is critical to deriving the Gini coefficient.

The Gini coefficient of an income (or any other kind of) distribution is the ratio of the area under the Lorenz curve of the distribution to the difference in area from a perfectly equal distribution (straight, diagonal line), or B/(A-B), where B is the Lorenz curve area and A is the perfect distribution area. The Gini coefficient is a value between 0 and 1. The closer this value is to 0, the more equal an income distribution is, and the closer it is to 1, the more inequal a distribution is.
