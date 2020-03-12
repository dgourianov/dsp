[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)
```python

import scipy.statsmu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

#How many people are between 5'10" and 6'1"?
# 5'10"= 70 inches, 6'1"=73 inches

dist.cdf(73*2.54)-dist.cdf(70*2.54)0.34274683763147457

0.34274683763147457
#about 34%

```

