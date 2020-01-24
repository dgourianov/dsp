[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
# calculating biased PMF of number of kids if children are surveyed
num_kids_biased=num_kids*num_kids.index
obs=num_kids_biased.sum()
nkb_pmf=num_kids_biased/obs
#calculating the mean of biased distribution
print ((nkb_pmf*nkb_pmf.index).sum())
print (nkb_pmf)
```
![plot](images/ex2plot.png)
