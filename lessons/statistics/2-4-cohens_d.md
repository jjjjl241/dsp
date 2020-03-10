[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```
def WeightDifference(live, firsts, others):
      
      mean0 = live.totalwgt_lb.mean()
      mean1 = firsts.totalwgt_lb.mean()
      mean2 = others.totalwgt_lb.mean()

      var1 = firsts.totalwgt_lb.var()
      var2 = others.totalwgt_lb.var()

      print('Mean')
      print('First babies', mean1)
      print('Others', mean2)

      print('Variance')
      print('First babies', var1)
      print('Others', var2)

      print('Difference in lbs', mean1 - mean2)
      print('Difference in oz', (mean1 - mean2) * 16)

      print('Difference relative to mean (%age points)', 
      (mean1 - mean2) / mean0 * 100)

      d = thinkstats2.CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
      print('Cohen d', d)
```
