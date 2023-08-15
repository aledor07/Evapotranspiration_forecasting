# Predicción de la evapotranspiración potencial mediante el empleo de Prophet y modelos clásicos

El modelo Prophet ha sido entrenado empleando el periodo de 2000-2023, para la estación de SIAR ubicada en el municipio de Puerto de La Cruz. Los resultados obtenidos indican un mejor ajuste a la serie temporal que los modelos clásicos ajustados. Más información en https://www.icia.es/icia/index.php?option=com_content&view=article&id=2742&Itemid=354&lang=es. 

La serie histórica se caracteriza por una marcada dispersión en los meses de verano, influenciada por los vientos Alisios y la orografía.

Los resultados obtenidos se muestran a continuación:

![Prophet 2](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/ffea5a01-beba-4f8b-a114-c9b15ba07e81)

![Prophet 1](https://github.com/aledor07/Evapotranspiration_forecasting/assets/86531400/180cab56-da88-450d-a54d-d31d81feadd5)


| **Coefficient** | **Value** |
|-----------------|-----------|
| MAE             | 0.49      |
| RMSE            | 0.64      |
| NSE             | 0.62      |
| R Squared       | 0.62      |

## Backtesting

El error absoluto medio porcentual al simular el periodo de 01/05/2022 al 26/05/2023 es del 22.30%, empleando Prophet como método predictivo. Al emplear la evapotranspiración registrada la semana anterior como predicción, el error se reduce hasta el 14.32% .
