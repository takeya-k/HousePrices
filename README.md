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

## Data Preprocessing
●　欠損値処理  
●　ダミー変数化

## Models
⓵ Linear Regression  
（評価指標）  
●　train-R² score：0.9418  
●　test-R² score：0.6218  

## Kaggle submission
（提出結果）  
|Model|Kaggle Score|
|-|-|
|Linear Regression|0.46171|

## Results
Linear Regression modelはKaggle Score 0.46171を示す、予測性能となった。  

## Environment
Python(pandas / scikit-learn / matplotlib)  
Kaggle  
