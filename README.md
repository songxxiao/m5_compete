# Sliver Solution (Top 2%) for Kaggle M5 Forecasting competitions

[![License: MIT](https://img.shields.io/badge/License-MIT-purple.svg)](https://opensource.org/licenses/MIT)

Kaggle M5沃尔玛销量时间序列预测竞赛 银牌方案(Top 2%) 

Xiao Song 宋骁

<https://xsong.ltd/en>     
[Kaggle profile](https://www.kaggle.com/rikdifos/)


[M5 Forecasting – Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy) – Top 103rd rank 2% (solo silver medal)   
[M5 Forecasting – Uncertainty](https://www.kaggle.com/c/m5-forecasting-uncertainty) – Top 18th rank 2% (solo silver medal)  


[Kaggle M5沃尔玛时间序列预测竞赛Baseline分享](https://mp.weixin.qq.com/s/E9vJwE5Vpa-TFrjeLyBT_A)   
[Kaggle M5 沃尔玛销量时间序列预测 竞赛总结](https://mp.weixin.qq.com/s/3JHWeYbh2uhqjw7IJoeOiQ)

## Summary

### Accuracy-Competition

+ FE: adding a `weekends` feature.

+ I used 4 single models:
    
    + time series split 3 fold cv - rmse loss function
    
    + [time series split 3 fold cv - poisson loss function](https://www.kaggle.com/rikdifos/timeseriessplit-cv-poisson)
    
    + time series split 3 fold cv - self-defined loss function
    
    + rolling prediction

+ Then I calculate all prediction's mean value, the I recode very tiny prediction to 0. Finally, I use a magic multiplier close to 1.

### Uncertainty-Competition

+ Use [public kernel](https://www.kaggle.com/szmnkrisz97/point-to-uncertainty-different-ranges-per-level) released by [KrisztianSz](https://www.kaggle.com/szmnkrisz97) to convert point prediction to uncertainty. I use accuracy final submission as input and get a single submission 1.

+ Use a [public kernel](https://www.kaggle.com/ulrich07/quantile-regression-with-keras) released by [Ulrich GOUE](https://www.kaggle.com/ulrich07) as a single submission 2.

+ Finally, I did an averaging from above 2 submission files and convert all negative prediction to 0.

# Happy Kaggling!










