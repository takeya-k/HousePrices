# House Prices Project in Kaggle(SalePrice Prediction)
## Overview
Kaggle House Pricesコンペティションにて、住宅/住宅関連情報から販売価格（SalePrice）を予測するモデルを構築した。

## Dataset
⓵使用データ  
●　train.csv  
●　test.csv  
●　sample_submission.csv  
●　data_description.txt

⓶目的変数  
●　SalePrice  

⓷説明変数  
●　元データ：79 explanatory variables  
●　ダミー変数化後：234 features  
●　特徴量エンジニアリング後：238 features

## Data Preprocessing
●　欠損値処理  
●　ダミー変数化  
●　特徴量エンジニアリング

## Models
⓵ Linear Regression  
（評価指標）  
●　train-R² score：0.9418  
●　test-R² score：0.6218  

⓶ Random Forest  
（評価指標）  
●　train-R² score(before implementing feature engineering)：0.9769    
●　test-R² score(before implementing feature engineering)：0.8391  
●　train-R² score(after implementing feature engineering)：0.9772    
●　test-R² score(after implementing feature engineering)：0.845

⓷ XGBoost Regressor  
（評価指標）  
●　train-R² score(after implementing feature engineering)：0.9998  
●　test-R² score(after implementing feature engineering)：0.8241  
●　train-R² score(after implementing feature engineering, max_depth=2)：0.964  
●　test-R² score(after implementing feature engineering, max_depth=2)：0.9003  
●　train-R² score(after implementing feature engineering, max_depth=2, n_estimators=200)： 0.9803  
●　test-R² score(after implementing feature engineering, max_depth=2, n_estimators=200)：0.9069  
●　train-R² score(after implementing feature engineering, max_depth=2, n_estimators=200, learning_rate=0.1)：0.9575  
●　test-R² score(after implementing feature engineering, max_depth=2, n_estimators=200, learning_rate=0.1)：0.911  

【実行内容】  
●　モデル比較  
●　特徴量エンジニアリングの追加  
●　ハイパーパラメーター調整    

## Kaggle submission　　
※ Evaluation Metric: RMSLE (Root Mean Squared Logarithmic Error)  
※ Lower score indicates better performance.  

（提出結果）  
|Model|Kaggle Score|
|-|-|
|Linear Regression|0.46171|
|Random Forest|0.15197|
|Random Forest adding feature engineering|0.14645|
|XGBoost Regressor|0.15166|
|XGBoost Regressor with max_depth=2|0.14415|
|XGBoost Regressor with max_depth=2, n_estimators=200|0.141|
|XGBoost Regressor with max_depth=2, n_estimators=200, learning_rate=0.1|0.14274|

## Results
Random Forest modelはLinear Regression modelよりも予測性能が高く、Kaggle Score 0.15197となり、feature engineering後はmodel性能の改善を認め、Kaggle Score 0.14645となった。  
XGBoost Regressor modelはハイパーパラメータ未調整でKaggle Score 0.15166となり、Random Forest modelよりも予測性能が低い結果となった。しかし、XGBoost Regressor modelのハイパーパラメータ調整後は予測性能の向上を認め、max_depth=2、n_estimators=200によるハイパーパラメーター調整後はKaggle Score 0.141となり、本プロジェクトにおいて最も高い予測性能を示した。また、learning_rate=0.1による調整も試行したがKaggle scoreの改善は認めなかった。

## Environment
Python(pandas / scikit-learn / matplotlib / xgboost)  
Kaggle  
