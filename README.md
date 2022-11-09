## Company_broke_Prediction
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
  - try 4 kinds of data cases  
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
