# Intermittent-demand-prediction-by-various-Croston-model
Use croston model to predict intermittent demand and compare various croston model.

## Crostonpackage.ipynb: python的croston套件
croston.fit_croston( input_data, predict_length, croston_model_type )
- croston_model_type: 'original', 'sba', 'sbj'
- Output: dictionary of forecast{'croston_model', 'croston_fittedvalues', 'croston_forecast'}

## function.ipynb: croston function by hand-made
Croston(input_data, predict_length, alpha )
- Output: dataframe of forecast{"Demand", "Forecast", "Period","Level", "Error"}

## transformCroston.ipynb: Various croston's transform methods
croston_method (input_data, alpha, n_steps)
alpha (default = 0.1 )
n_steps: number of predict length ( default = 1)
Output:  v_i: parameter of demand size ()
         q_i: parameter of inter-demand interval ()
         f_i: predict data
-         
sba_method (input_data, alpha, n_steps)



同croston_method



-         
sbj_method (input_data, alpha, n_steps)



-         
同croston_method



-         
tsb_method (input_data, alpha, beta, n_steps)



beta (default
= 0.1)



其餘同croston_method



-         
hes_method (input_data, alpha, n_steps)



同croston_method



-         
les_method (input_data, alpha, n_steps) 



同croston_method



-         
ses_method (input_data, alpha, n_steps)



同croston_method



 



deepCroston.ipynb: deeprenewal套件中的croston function



-         
用法參照Deeprenewal



-         
CrostonForecastPredictor(



Freq =
‘1D’,          # 時間區間



                      prediction_length ,   #
預測長度 



                      variant = 'original',    



#croston
model type: original, sba, sbj



                      no_of_params=2



                      )



Output: predictor



 



-         
corston_predictor(
input_training_data )



Output: forecast data
