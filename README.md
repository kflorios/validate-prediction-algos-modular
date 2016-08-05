# validate-prediction-algos
-modular

To run the R code you will need:

1. A working installation of >R3.0

4. packages 'tseries','nnet','xtable','pracma','matrixStats','e1071','randomForest','ROCR','verification' in R installed


Run has been checked in a windows 64 machine.


Guideline

Put

a) Script_Monte_SHYKJG1_MX_Modular.R  (R main)
b) functions_Monte_SHYKJG1_MX_Modular.R (R functions)
c) dataset_for_wp3_v3.txt (input file)

in same directory and change lines 6-7 in R main with root = current working directory

Run Script_Monte_SHYKJG1_MX_Modular.R in RStudio
The script takes 1-2 mins to run.

If you change line 21 in R main, such that 
for (m in 1:1) becomes
for (m in 1:R)

it should take one hour to run, since it will perform R=200 monte carlo iterations.

In the current directory many files are produced.

The final result is the skill score statistics ACC, TSS, HSS for all methods which is also produced as a latex file,
and displayed at the console tab window of RStudio with latex code.

The methods are
0: Neural network
1: Linear regression
2: Probit regression
3: Logit regression
4: Random Forest
5: Support vector Machine

Several Function are used and the Code is Modular.
Fore example, 
fc_lm() : to estimate a lm()
fc_nnet() : to train a nnet()

fc_lm_predict() : to predict for a lm()
fc_nnet_predict() : to predict for a nnet()

fc means for (F)lare(C)ast.