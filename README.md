# Prediction of the potential evapotranspiration using Prophet and classical models

The Prophet model has been trained using the period 2000-2023, for the SIAR station located in the municipality of Puerto de La Cruz. The results obtained indicate a better fit to the time series than the classical fitted models. More information at https://www.icia.es/icia/index.php?option=com_content&view=article&id=2742&Itemid=354&lang=es. 

The historical series is characterised by a marked dispersion in the summer months, influenced by the trade winds and the orography.

The results obtained are shown below:

![Prophet 1](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/d2406806-e17a-4cb3-a365-6f3dd930768c)

![Prophet 2](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/cd6ff69d-ceab-4cd0-a287-fbcc348e4b7a)

##### <em> 95% confidence intervals </em>



| **Coefficient** | **Value** |
|-----------------|-----------|
| MAE             | 0.49      |
| RMSE            | 0.64      |
| NSE             | 0.62      |
| R Squared       | 0.62      |

## Backtesting

The mean absolute percentage error when simulating the period from 01/05/2022 to 26/05/2023 is 22.30%, using Prophet as the prediction method. When using the evapotranspiration recorded the previous week as a prediction, the error is reduced to 14.32%.
