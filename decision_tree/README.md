# 決策樹迷你項目

在這個項目中，我們使用決策樹再次將郵件進行分類，啟動代碼是decision_tree/dt_author_id.py。

## 第一部分：讓決策樹運行起來

構建一個決策樹運行的分類器，設置 `min_samples_split`=40。開始訓練之前，這可能需要一些時間。我們的問題是，這個決策樹的精確度是多少？

## 第二部分：加速

在SVM 迷你項目中，你會發現參數調節能顯著加速機器學習算法的訓練時間。一般的規律是參數可以調整算法的復雜度，通常更加復雜的算法意味著運行得更慢。另外一個方法是通過訓練/測試所使用的特征數量控制算法的復雜度。算法中可用的特征越多，出現復雜擬合的可能性就越大。我們會在“特征選擇”的課程中詳細討論這個問題，不過現在你可以先預覽一下。

## 思考一下

* 從你的數據中找出特征的數量，數據是以numpy 數組的形式排列的，其中數組的行數代表數據點的數量，列數代表特征的數量；為了提取這個數值，可以寫一行這樣的代碼`len(features_train[0])``
* 加入 tools/email_preprocess.py，會看到這樣的代碼：`selector = SelectPercentile(f_classif, percentile=1)`，將percentile從10 改為1。
* 現在的特征數量是多少呢？
* 你認為SelectPercentile 起到什麼作用？其他所有的都不變的情況下，賦予percentile 的值較大是否得到一棵更加復雜的或者簡化的決策樹？
* 注意訓練時間的長短會取決於我們訓練的特征的數量。
* 當percentile
* 等於 1 時，準確度是多少？

翻译：Iris 2016 年 9 月
