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

【実行内容】  
●　モデル比較  
●　特徴量エンジニアリングの追加

## Kaggle submission　　
※ Evaluation Metric: RMSLE (Root Mean Squared Logarithmic Error)  
※ Lower score indicates better performance.  

（提出結果）  
|Model|Kaggle Score|
|-|-|
|Linear Regression|0.46171|
|Random Forest|0.15197|
|Random Forest adding feature engineering|0.14645|

## Results
Random Forest modelはLinear Regression modelよりも予測性能が高く、Kaggle Score 0.15197となった。
さらに、feature engineering後はmodel性能の改善を認め、Kaggle Score 0.14645となった。

## Environment
Python(pandas / scikit-learn / matplotlib)  
Kaggle  
