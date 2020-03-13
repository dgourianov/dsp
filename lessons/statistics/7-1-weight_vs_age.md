[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])```python
import matplotlib.pyplot as plt 
import seaborn as sns

sns.scatterplot(x=live['agepreg'], y=live ['totalwgt_lb'])
plt.ylabel('Total weight')
plt.xlabel( 'Age' )
plt.show()


