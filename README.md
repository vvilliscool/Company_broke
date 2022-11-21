## Company_broke_Prediction Project Summary
### This is made during Internship at company(related to finance and investment) 

  
##
 2022-09-29 : Starting date  
  - Purpose : improving corporate bankruptcy prediction  
  - Models tried : RandomForest, Catboost, LGBM, XGB


##
2022-10-06  
  - new data file & new features  
  - Purpose : trying from preprocess to calculate (value * feature importance)


##
2022-10-12  
  - search catboost  
  - drop duplicate  
  - search how to class_weight to catboost (for reducing type 1,2 error)


##
2022-10-27  
  - try 4 kinds of data cases :  
    1) change just lab type  
    2) change lab type and replace 0 to mean of land price  
    3) change lab type and qcut 10  
    4) change lab type, replace 0 to mean of land price and qcut 10  

  - all of these try two (1. original land price 2. logged land price)


##
2022-11-09
1. add more continuous features and removes some features(existed)
2. try AutoML - H2O : install failed
              - AutoGluon : install success
3. AutoGluon
      - by point of Accuracy  : WeightedEnsemble_L2 (0.9896)
      - by point of Precision : NeuralNetTorch  (0.815789)
      - by point of Recall    : KNeighborsDist  (0.623613)
      

##
2022-11-10  
  - using Sklearn - Scalers :  
    - StandardScaler (a.k.a good for Classification)  
    - MinMaxScaler (a.k.a good for Regression)  
    
  - try KNN (with StandardScaler) at the point of accuracy, precision and recall : 
    - accuracy : K = 2, 4  ----  17,18
    - precision : K = 2,4,  ---  10 
    - recall : K = 1, 3, 5 ...  (odd numbers but decreasing)

  - try KNN (with MinMaxScaler) at the point of accuracy, precision and recall : 
    - accuracy : K = 2, 4  ---  10
    - precision : K = 2, 4  ---  10
    - recall : K = 1, 3, 5 ...  (odd numbers but decreasing)
    
    
##
2022-11-11  
  - for documentation of these results:
    - making presentation more clear
    - make sure the meaning of table corret and clear (for everyone even first time seeing)
    - using layouts





### 생각의 흐름 및 방안 도출 과정
전체 속성 중 원소 수 10개의 조합 -> 메모리 오류 -> 속성을 절반으로 나눠 각각 원소 수 5개의 조합을 만들어 이어붙이기 (순차 계산 및 추출)  
--> 대표성을 생각하여 random을 도입 --> 앞 5개원소 조합 random 선택, 뒤 5개원소 조합 random 선택으로 다양성, 무작위성 증가  
--> 10개의 원소를 random하게 뽑아 계산되게하기 (원소 자체로하면 메모리가 크니, 숫자를 뽑아 index 조회로 list 만들기)
