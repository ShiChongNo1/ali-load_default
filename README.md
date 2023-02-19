# 阿里云贷款违约检测
## 1. 数据集
    https://tianchi.aliyun.com/competition/entrance/531830/information
## 2.特征处理
    * 异常值的处理（约2万条左右，总体训练集:80万)
    * 特征交互
    * 业务逻辑
## 3. 模型选择
    * 删除异常值后
        * catboost  score: 0.3727   5折交叉验证分数：【'cat_score_mean': 0.7357131828581313, 'cat_score_std': 0.0011723401351547054】
        * lgbm      score: 0.3727   5折交叉验证分数：【'lgb_score_mean': 0.7355417140621585, 'lgb_score_std': 0.0010119941056547825】
        * xgb       score: 0.3742   5折交叉验证分数：【'xgb_score_mean': 0.7370806928333352, 'xgb_score_std': 0.0009682665927953546】
    * 有意思的是我们这里的catboost和lgbm得到了相同的分数，针对于本题而言：在未进行异常的、特征工程的数据的catboost的性能分数是 0.74左右。为什么会有这种情况呢？
        * 异常值：
## 4. 调参
## 5. 模型融合