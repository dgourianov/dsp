[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

```python

import pandas as pd


sam_pd=pd.DataFrame(sample)
print('mean:', sam_pd.mean(),'\n','median:',  sam_pd.median(),'\n','skewness', sam_pd.skew())

mean: 0    74278.707531
dtype: float64 
 median: 0    51226.933066
dtype: float64 
 skewness 0    4.949981
dtype: float64

sam_pd.shape
(122458, 1)

#calculating what fraction of the households have income below mean
len(sam_pd[sam_pd.iloc[:,0]<74278])/122458
0.660005879566872

```




