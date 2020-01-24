[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)
Exercise: Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample.

Use the NSFG respondent variable numkdhh to construct the actual distribution for the number of children under 18 in the respondents' households.

Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.

Plot the actual and biased distributions, and compute their means.

```python
print(resp['numkdhh'].mean()
1.024205155043831
#actual distribution (PMF) of number of kids per respondent' households
num_kids=resp['numkdhh'].value_counts()
num_kids_pmf=num_kids/num_kids.sum()
print(num_kids_pmf)
0    0.466178
1    0.214052
2    0.196258
3    0.087139
4    0.025644
5    0.010729
Name: numkdhh, dtype: float64

# calculating biased PMF of number of kids if children are surveyed
num_kids_biased=num_kids*num_kids.index
obs=num_kids_biased.sum()
nkb_pmf=num_kids_biased/obs
#calculating the mean of biased distribution
print ((nkb_pmf*nkb_pmf.index).sum())
print (nkb_pmf)
2.403679100664282
0    0.000000
1    0.208993
2    0.383240
3    0.255238
4    0.100153
5    0.052376
dtype: float64

```
![plot](images/ex2plot.png)
