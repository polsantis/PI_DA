# Proyecto de Análisis de Datos de Criptomonedas 'Stable Coins'

Bienvenido al Proyecto de Análisis de Datos de Stable Coins. En este proyecto, realizamos un análisis exploratorio de las Stable Coins utilizando la API CoinGecko. A continuación, se detallan los pasos realizados, los resultados obtenidos y los KPIs utilizados en el análisis.

## Requisitos

- Python 3.7+
- Librerías: pandas, seaborn, matplotlib, datetime, time, pycoingecko

## Descripción

El mercado de las criptomonedas ha experimentado un crecimiento exponencial y una creciente adopción a nivel mundial. Este proyecto simula el papel de un Analista de Datos en una empresa financiera que busca comprender mejor el comportamiento y la evolución de las criptomonedas estables o 'Stable Coins'. Se utiliza la API CoinGecko para obtener y analizar datos relevantes.

## KPIs

1. **Market Capitalization (Capitalización de mercado):**

La capitalización de mercado es una medida que indica el valor total de una criptomoneda en circulación en un momento determinado. Se calcula multiplicando el precio actual de la criptomoneda por su oferta circulante. Es un indicador importante para comprender la magnitud y la relevancia de una criptomoneda en el mercado. Las criptomonedas con una alta capitalización de mercado suelen ser consideradas más establecidas y prominentes en comparación con las de capitalización de mercado más baja.

2. **ATR (Average True Range) - Rango Verdadero Promedio:** 

El ATR es un indicador de volatilidad que mide la diferencia entre el precio máximo y mínimo en un período determinado. Proporciona una medida de la volatilidad real del mercado, teniendo en cuenta las brechas y limitaciones del precio. Un ATR más alto indica una mayor volatilidad, mientras que un ATR más bajo sugiere menor volatilidad. El ATR es útil para los traders que desean establecer stop-loss y take-profit en función de la volatilidad actual.

3. **RSI (Relative Strength Index) - Índice de Fuerza Relativa:** 

El RSI es un indicador de momentum que evalúa la velocidad y el cambio de los movimientos de los precios. RSI oscila entre 0 y 100 y se utiliza para identificar condiciones de sobrecompra (RSI cerca de 70 o superior) y sobreventa (RSI cerca de 30 o inferior). Un RSI alto puede indicar que un activo está sobrecomprado y podría haber una reversión a la baja, mientras que un RSI bajo puede sugerir que un activo está sobrevendido y podría haber una reversión al alza.

## Pasos Realizados

1. **Importar Bibliotecas:** Importamos las bibliotecas necesarias, incluyendo pandas, seaborn, matplotlib, datetime, time y pycoingecko.

2. **Conexión a la API CoinGecko:** Establecemos una conexión con la API CoinGecko utilizando el módulo `CoinGeckoAPI`.

3. **Verificación de Disponibilidad de la API:** Verificamos la disponibilidad de la API mediante `cg.ping()`.

4. **Obtención de Categorías de Monedas:** Utilizamos `cg.get_coins_categories_list()` para obtener la lista de categorías de monedas.

5. **Filtrado de Criptomonedas Estables:** Filtramos las criptomonedas estables de la lista de categorías utilizando `str.contains()`.

6. **Obtención de Datos de Capitalización de Mercado:** Utilizamos `cg.get_coins_markets()` para obtener los datos de capitalización de mercado de las criptomonedas estables en USD.

7. **Creación de DataFrame de Criptomonedas Estables:** Seleccionamos los 10 primeros resultados y creamos un DataFrame con la información relevante: nombre, precio actual, capitalización de mercado y suministro circulante.

8. **Visualización de Capitalización de Mercado:** Creamos un gráfico de barras que muestra la capitalización de mercado de las criptomonedas estables.

9. **Visualización de Precios Actuales:** Creamos otro gráfico de barras que muestra los precios actuales de las criptomonedas estables.

10. **Generación de Gráfico Circular:** Creamos un gráfico circular (pie chart) que muestra la distribución de la capitalización de mercado entre las criptomonedas estables.

11. **Cálculo y Visualización de Porcentajes:** Calculamos y mostramos el porcentaje de la capitalización de mercado de cada criptomoneda estable.

12. **Obtención de Datos de Precios Históricos:** En el segundo notebook, utilizamos `cg.get_coin_ohlc_by_id()` para obtener datos de precios históricos (OHLC) de nuestra selección de criptomonedas estables en un período de 180 días.

13. **Cálculo de ATR y RSI:** Calculamos el ATR (Average True Range) y el RSI (Relative Strength Index) para cada una de las criptomoneda estable seleccionadas para el análisis, utilizando sus datos de precios históricos.

14. **Creación del DataFrame Final:** Creamos un DataFrame consolidado que incluye los datos de precios históricos, ATR y RSI para todas las 'Stable Coins' selecionadas.

15. **Exportación de Datos:** Exportamos los datos del DataFrame final a un archivo CSV llamado 'olhc_monedas.csv'.

16. **Creación de Dashboard Interactivo:** En el archivo PI_II_DA.pbix, comenzamos a desarrollar un dashboard interactivo. Este dashboard presentará gráficos interactivos que complementan el análisis de las criptomonedas estables y facilitan la comprensión de los resultados.


## Conclusiones

*Market Capitalization*

Basándonos en el análisis desarrollado en el archivo PI_II_DA.ipynb en el cual hacemos especial énfasis en el análisis de capitalización de mercado para las stablecoins seleccionadas, podemos observar lo siguiente:

Tether (USDT) es la stablecoin líder con una capitalización de mercado del 68.12%. Esto indica que Tether es ampliamente adoptada y utilizada en el mercado de criptomonedas.

USD Coin (USDC) ocupa el segundo lugar con un 21.25% de la capitalización total. Al igual que Tether, USD Coin es una stablecoin respaldada por dólares estadounidenses, lo que la hace atractiva para su uso en el comercio de criptomonedas.

Dai (DAI) representa un 3.21% del mercado de stablecoins. Dai es una stablecoin descentralizada respaldada por garantías criptográficas y es parte del ecosistema MakerDAO.

Binance USD (BUSD) tiene una participación del 2.74%. Esta stablecoin es emitida por la plataforma de intercambio Binance y se utiliza como un puente entre las operaciones en Binance y otras plataformas.

TrueUSD (TUSD) tiene una participación del 2.25%. Similar a otras stablecoins, TrueUSD está respaldada por dólares estadounidenses en una relación de 1:1.

Frax (FRAX) representa el 0.66% del mercado. Frax es una stablecoin algorítmica que utiliza un protocolo descentralizado para mantener su estabilidad en valor.

USDD y Pax Dollar (USDP) tienen un 0.59% y 0.41% respectivamente. Aunque tienen una participación relativamente pequeña, siguen siendo relevantes en el panorama de las stablecoins.

PAX Gold (PAXG) y Tether Gold (XAUT) tienen una participación del 0.39% y 0.38% respectivamente. Estas stablecoins están respaldadas por oro y ofrecen una alternativa respaldada por activos físicos en el mundo de las criptomonedas.

En general, Tether (USDT) y USD Coin (USDC) dominan el mercado de stablecoins, seguidos por otras opciones populares y novedosas como Dai, Binance USD y TrueUSD. Estas stablecoins juegan un papel importante en la facilitación de transacciones en el mundo de las criptomonedas, brindando una alternativa a la volatilidad inherente de muchas criptomonedas tradicionales.

...

## Uso Adicional

Este proyecto puede servir como punto de partida para un análisis más profundo de las criptomonedas estables, incluyendo investigaciones sobre su adopción, casos de uso y volatilidad en comparación con otras criptomonedas y activos financieros.

## Dashboard

Además, se ha desarrollado un dashboard interactivo utilizando Power BI. Este dashboard presenta gráficos interactivos que complementan el análisis de las criptomonedas estables y facilitan la comprensión de los resultados.

## Referencias

- Documentación de CoinGecko API: [CoinGecko API Documentation](https://www.coingecko.com/en/api)

## Autor

Santisteban, Pablo A.

---

Sentite libre de clonar este repositorio y utilizar el código y los resultados para tus propios análisis y aprendizaje. ¡Explora el emocionante mundo de las criptomonedas estables y los datos!

