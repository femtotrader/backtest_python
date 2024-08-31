# backtest_python

FMZ backtest engine python package
support python2 and python3, support Windows, Linux, Mac

## install

```
pip install https://github.com/fmzquant/backtest_python/archive/master.zip
```

OR

```
pip3 install https://github.com/fmzquant/backtest_python/archive/master.zip
```

## simple example
```python
'''backtest
start: 2022-02-19 00:00:00
end: 2022-03-22 12:00:00
period: 15m
exchanges: [{"eid":"Binance","currency":"BTC_USDT","balance":10000,"stocks":0}]
'''
from fmz import *
task = VCtx(__doc__) # initialize backtest engine from __doc__
print(exchange.GetAccount())
print(exchange.GetTicker())
print(task.Join(True)) # print backtest result
task.Show() # or show backtest chart
```

The config string can be generated automatically by saving the backtest configuration in the strategy edit page.

配置字符串可以通过策略编辑界面里的保存回测配置来自动生成

![meta](https://www.fmz.com/upload/asset/aa67494fc6306759753385bf7634ee4cd437f3f2.png) 
 
## api
https://www.fmz.com/api

