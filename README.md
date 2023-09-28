# Prediction of the potential evapotranspiration using Prophet and classical models

The Prophet model has been trained using data from three weather stations located at different areas in the Tenerife island. The results obtained indicate a better fit to the time series than the classical fitted models. 

The historical series is characterised by a marked dispersion in the summer months, influenced by the trade winds and the orography.

The results obtained are shown below:

### Puerto de La Cruz

![Prophet 1](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/d2406806-e17a-4cb3-a365-6f3dd930768c)

### Las Galletas

![galletas](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/d542a42c-c63d-42cd-82ba-9bf3393d8cc3)


### Pajalillos - Valle Guerra

![pajalillos](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/4186be0a-00f8-4b93-9a59-599f9961ed64)


##### <em> 95% confidence intervals </em>



| **Coefficient** | **Puerto de La Cruz** | **Las Galletas** | **Pajalillos** |
|:---------------:|:---------------------:|:----------------:|:--------------:|
| **MAE**         | 0.49                  | 0.51             | 0.52           |
| **RMSE**        | 0.64                  | 0.67             | 0.69           |
| **NSE**         | 0.62                  | 0.65             | 0.61           |
| **R Squared**   | 0.62                  | 0.65             | 0.62           |

Several tests were conducted using additional regressors but no improvement in the results was observed.

## Backtesting

The mean absolute percentage error when simulating the period from 01/05/2022 to 26/05/2023 at daily scale and 7 days horizon is:

| **Coefficient** | **Puerto de La Cruz** | **Las Galletas** | **Pajalillos** |
|:---------------:|:---------------------:|:----------------:|:--------------:|
| **MAPE**        | 22.30                 | 19.29            | 15.87          |


## Prophet vs Previous week demand for a week ahead forecasting

The difference between using the previous week evapotranspiration and Prophet for a week ahead forecasting is shown below. The forecasted period ranges from 05/2022 to 05/2023.

![Puerto de la cruz diferencias](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/99dee836-8a83-4740-ae69-b0ad128052e8)

![Las Galletas](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/9942fe8d-8136-46cb-9cb8-5a7486b179ed)


![Pajalillos Dif](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/01d03b9e-3fc1-4efe-8344-6bb0f2df023e)


The graph shows that both methods have an accuracy error of less than 20% most of the year. The accuracy offered by Prophet in the months with the highest demand, compared to the previous week's method, stands out. 


| **Method**        | **Coefficient** | **Puerto de La Cruz** | **Las Galletas** | **Pajalillos** |
|:-----------------:|:---------------:|:---------------------:|:----------------:|:--------------:|
| **Prophet**       | MAPE            | 11.79                 | 11.72            | 8.47           |
|               | Sum (mm)        | 1011.57               | 1173.12          | 1278.71        |
| **Previous week** | MAPE            | 14.20                 | 12.26            | 11.14          |
|               | Sum (mm)        | 1047.08               | 1262.17          | 1338.71        |
| **Historical**    | Sum (mm)        | 1045.64               | 1264.17          | 1348.87        |

## NeuralProphet

The results obtained using the minimum tempearature and solar radiaton as regressors are shown below:


| **Coefficient** | **Puerto de La Cruz** | **Las Galletas** | **Pajalillos** |
|:---------------:|:---------------------:|:----------------:|:--------------:|
| **MAE**         | 0.46                  | 0.47             | 0.50           |
| **RMSE**        | 0.59                  | 0.63             | 0.70           |
| **NSE**         | 0.68                  | 0.70             | 0.62           |
| **R Squared**   | 0.68                  | 0.70             | 0.62           |
