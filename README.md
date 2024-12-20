# Remaining Useful Life Prediction Using NASA Battery Data Set

## 1️⃣ Overview
### ◽ Objective
   - [x] NASA에서 제공하는 4개 셀 리튬이온 배터리 데이터를 명세하고 분석하여 데이터를 이해한다.
   - [x] 데이터 전처리 및 학습에 알맞은 형태로 가공한다.
   - [x] AI(ML/DL)기반의 다양한 방법론(알고리즘,모델)을 적용한 배터리 잔존수명예측 모델링을 진행한다.
---
### ◽ Development Environment
page_type | languages | products
:------:|:------:|:------:
　　　　　`Dev`　　　　　|　　`pyspark`　`python`　　|`azure`　`azure-databricks`
---
### ◽ NASA PCoE Battery Data
<p align="left"> <img src="https://user-images.githubusercontent.com/88306533/128735382-30fec59a-fcb7-4763-9f89-46c658035fa5.png" width="75%" height="75%"></img></p>

> **Download URL** - https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/
---
<br>

## 2️⃣ PreRequirement
### ◽ Understanding Data 
- SOH : State of Health
- RUL : Remaining Useful Life
- EOL : End of Life

### ◽ Data Structure 
 - ❶ cycle: top level structure array containing the charge, discharge and impedance operations

   |　cycle　|`⇦ Complex Data Structure( Nested Data )` |
   |:------:|:------:|
   
   ⏬

 - ❷ type: operation type, can be charge, discharge or impedance
 - ❸ Data: Nested Data Structure(Many Variables)

   |type | ambient_temperature | time | data|
   |:------:|:------:|:------:|:------:|
   |charge|`24℃`|`yyyy-MM-dd HH:mm:ss.SSSSSS`|`data`|
   |discharge |''|''|''|
   |impedance |''|''|''|
   
---
<br>

## 3️⃣ Methodology
### ◽ Part1 : Convert .mat to Dataframe
   > - [Convert .mat to Dataframe.ipynb](https://github.com/YJPark0421/LSTM-Analytics-NASA-Battery-LTV-Prediction/blob/master/Code/Preprocessing-Setup.ipynb)
### ◽ Part2 : EDA(Exploratory Data Analysis)
   > - [EDA-Battery-Data.ipynb](https://github.com/YJPark0421/LSTM-Analytics-NASA-Battery-LTV-Prediction/blob/master/Code/EDA-Battery-Data-v0.1.ipynb) 
### ◽ Part3 : Modeling
   > - [LSTM_Based_SOH_Prediction.ipynb](https://github.com/YJPark0421/LSTM-Analytics-NASA-Battery-LTV-Prediction/blob/master/Code/LSTM_Based_SOH_Prediction_v0.1.ipynb)
   > - [SVM_Based_SOH_Prediction.ipynb](https://github.com/YJPark0421/LSTM-Analytics-NASA-Battery-LTV-Prediction/blob/master/Code/SVM_Based_SOH_Prediction_v0.1.ipynb)
### ◽ LSTM Based Model Prediction Result Example
   > <p align="left"> <img src="https://user-images.githubusercontent.com/88306533/128865333-b2d2fc15-a00e-47db-a391-162ba7d65dfe.png" width="55%" height="55%"></img></p>
### ◽ Understanding LSTM(Long Short-Term Memory)
   > <p align="left"> <img width="55%" height="55%" alt="rnn-lstm-cell" src="https://user-images.githubusercontent.com/88306533/129383011-a8bbea44-8cba-440c-a0de-a80e840689e6.png"></img></p>

   > **Read a Blog** - http://colah.github.io/posts/2015-08-Understanding-LSTMs/
### ◽ Understanding SVM(Support Vector Machines)
   > **Watch a Youtube** - https://www.youtube.com/watch?v=eHsErlPJWUU
---
<br>

## 4️⃣ Reference
> **URL①** - https://ieeexplore.ieee.org/document/8967059<br>
