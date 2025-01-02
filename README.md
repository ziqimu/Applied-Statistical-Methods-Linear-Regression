### Abstract
Sleep plays a vital role throughout mammals’ life and maintains their good health. Our group wants to
explore variables that influence mammals’ total sleep time. Our first case focuses on the correlation between
sleep exposure and total sleep time. We mainly use Kruskal-Wallis Test and multiple comparisons test and
found out that sleep exposure does significantly correlate with total sleep time. In our second case, we are
trying to predict the total sleep time based on brain weight, max life span, and predation index. Using
multiple regression models and checking assumptions, we successfully fit a regression line
yhat = 15.4471 − 0.1113 * x_maxlifespan − 0.8986 * x_predation2 − 4.8357 * x_predation3 − 3.0913 * x_predation4 − 6.6951 * x_predation5
to predict mammals’ total sleep time.

## Background and Data Description

The data set we want to explore collected brain weight, body weight, life span, gestation time, time sleeping,
predation, and danger indices for 62 mammals. In our study, we mainly focus on brain weight, maximum
life span, predation index, sleep exposure index, and total sleep.

1. Brain weight is the mammals’ brain weight in g, ranging from 0.14g to 5712g with mean value 317.5.
Boxplot and histogram show that this data skews to the right and have extreme outliers. However, it
is normal to have outliers in this case since mammals’ brain size and weight differ a lot.

2. Maximum life span is the length of time for which mammals live in years. This variable ranges from 2
years to 100 years. Both boxplot and histogram are right skewed and extreme outliers exist, indicating
that this data is not normal. However, whether this distribution is normal or not is not important
since we use max life span as a variable in Q|QQC case, where normality assumptions is checked via
the histogram of total sleep time and qq plot of residuals.

3. Predation index means the probability that one organism is preyed and killed by another. This index is
a categorical variable scores from 1 to 5, 1 represents least likely to be preyed upon and 5 means this
mammal is most likely to be preyed upon.

4. As another categorical variable, sleep exposure index also scores from 1 to 5, 1 means this mammal is
least exposed and sleeps in a well-protected den. 5 means it’s most exposed.

5. Total sleep represents the mammals’ total sleep in hours. Total sleep ranges from 2.6 hours to 19.9
hours, with mean value 10.35 hours and median 10.3 hours. The mean and median are pretty close to
each other, indicating a normal distribution, without any outliers.

## Getting the Dataset
Access data from Kaggle: 

[Mammal Sleep Dataset on Kaggle](https://www.kaggle.com/datasets/mathurinache/sleep-dataset)

## Conclusion

### 1. Case CQ
For the CQ (categorical and quantitative) case analysis,  we are exploring if the sense of security would
correlate with total sleep time. We divide mammals into “low exposure” and “high exposure” according to their sleep exposure index, and calculate the bi-serial correlation between total sleep time and exposure level. The bi-serial correlation is -0.7474052, indicating a
negative and moderately strong relationship. The p-value of the correlation test is 2.947115e-05, which is smaller
than α. Thus we have enough evidence to reject H0 and conclude that this Biserial correlation is significant,
and can happen at the population level based on our sample.

### 2. Case QQQC
In this case, we are trying to predict the total sleep time based on brain weight, max life span, and predation index. AIC for forward elimination and stepwise selection are both 283.14995, whereas AIC is 299.6893 for backward selection. Forward elimination and stepwise selection both reached the same model, and this model had a lower AIC than the model from backward selection. Based on this, the preferred model for total sleep time
is based on max_life_span and predation_index.

Thus, the regression model is 
**yhat = 15.4471 − 0.1113 * x_maxlifespan − 0.8986 * x_predation2 − 4.8357 * x_predation3 − 3.0913 * x_predation4 − 6.6951 * x_predation5**



# Tools I use
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/r/r-original.svg" title="R" alt="R" width="40" height="40"/>&nbsp;
 
</div>


