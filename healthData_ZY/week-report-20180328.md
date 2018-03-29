﻿# 健康体检数据周报20180326--xgboost建模gbtree完善

## 增加年龄和性别feature
* 选取决定代谢综合征的指标作为feature，次年结果y2作为label
* auc=0.934；nrounds.best=87（达到过一次0.934，后来几次都是0.93了）
* feature Gain由大到小 age, TG, FBG, HDL, SBP, DBP, BMI, TLDL, XINGBIE
* 相较于无年龄性别：auc=0.925；feature Gain由大到小 DBP，HDL, TG, FBG, TLDL, SBP, BMI

## 利用df6N跑模型（y=0）
* auc=0.884；error=0.074
* 阈值0.08，tpr=0.834

## 利用df6Y跑模型（y=1）
* auc=0.745；error=0.277

## 问题
* 年龄和性别转为factor则建模选取数据失败
* df5和df6的feature Gain，其中BMI占比差距大，feature顺序不同

## 待判断
* feature TLDL是否会增加准确性

## 计划
* 要不要增加feature看看呢？增加些什么捏？

