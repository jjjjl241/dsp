[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

Mean of actual distribution = 1.024205155043831  
Mean of biased distribution = 2.403679100664282

Actual vs biased plot:

![Actual vs biased plot](https://github.com/syntheticjohn/dsp/blob/syntheticjohn/img/Actual%20vs%20biased%20plot)

```
resp = nsfg.ReadFemResp()

pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Number of children', ylabel='PMF')

biased = BiasPmf(pmf, label='biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased])
thinkplot.Config(xlabel='Number of children', ylabel='PMF')

pmf.Mean()

biased.Mean()
```
