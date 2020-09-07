# Z-Score Explanation
### Using Z-Score between Fantasty Football Leagues to have a true relative score
#### By Alex Jerome

## The Need

Last year we had 3 Fantasy Football leagues that we wanted have fight against each other. For the finals, we picked a top 8 bracket from the top 8 "Best Performers".

We determined the "Best performers" through Z-Score - a metric that would work between leagues.

## Is it Valid?

Now, ~1 year after the Z-Score introduction, is it a valid metric?

In short, **yes** (I think).

## Proving it

Just some context, I got degrees in Marketing & CS. I don't know much about statistics. If I'm wrong, please reach out to me to correct this. I'm excited to learn!

### What is Z-Score?

Z-score is a measure of standard deviations from the mean. The general formula is: $Z = {\frac{x-\mu}{\sigma}}$ where $x$ is the observed value (your sum of "points for"), $\mu$ is the individual league's "points for" mean, and $\sigma$ is the standard deviation of the individual league's "points for" metric.

### Using the Z-Test.

According to the University of Oregon, [Z-Score is valid as long as the Z-Test says the means are about the same](http://homework.uoregon.edu/pub/class/es202/ztest.html). "About the same" is a Z-Test number whose absolute value is less than two.

The formula for the Z-Test is: $Z = {\frac{\bar X_1 - \bar X_2}{\sqrt{\sigma^2_{X_1}+\sigma^2_{X_2}}}}$ where $\bar X_1$ is the mean value of sample one, $\bar X_2$ is the mean value of sample two, $\sigma_{X_1}$ is the standard deviation of sample one divided by the square root of the number of data points, $\sigma_{X_2}$ is the standard deviation of sample two divided by the square root of the number of data points.

I used data from week 13 when all people were still involved. They are rounded to the nearest whole number.

| League Number | Mean | Std. Deviation |
|---------------|------|----------------|
| 1             | 1476 | 180            |
| 2             | 1448 | 100            |
| 3             | 1451 | 142            |

Therefore, the resulting test combinations are:

| League Number | Absolute Value of Test Score |
|---------------|------------------------------|
| 1 & 2         | 0.136                        |
| 2 & 3         | 0.023                        |
| 3 & 1         | 0.105                        |

Seeing as all three are much less than two, their means are approximately the same, and the Z-Score methodology should be valid.



