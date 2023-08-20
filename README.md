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

The mean absolute percentage error when simulating the period from 01/05/2022 to 26/05/2023 at daily scale and 7 days horizon is 22.30%.


## Prophet vs Previous week demand for a week ahead forecasting

The difference between using the previous week evapotranspiration and Prophet for a week ahead forecasting is shown below. The forecasted period ranges from 05/2022 to 05/2023.

![Puerto de la cruz diferencias](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/99dee836-8a83-4740-ae69-b0ad128052e8)

The graph shows that both methods have an accuracy error of less than 20% most of the year. The accuracy offered by Prophet in the months with the highest demand, compared to the previous week's method, stands out. On the other hand, an overestimation of evapotranspiration can be seen for the months of October and November obtained by Prophet.


| **Method**    | **Coefficient** | **Value** |
|---------------|-----------------|-----------|
| Prophet       | MAPE            | 11.79     |
|               | Sum (mm)        | 1011.57   |
| Previous week | MAPE            | 14.20     |
|               | Sum (mm)        | 1047.08   |

The historical evapotrasnpiration amount registered in this period is 1045.64 mm.