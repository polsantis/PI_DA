# Proyecto de Análisis de Datos de Criptomonedas Estables

Este proyecto tiene como objetivo realizar un análisis exploratorio de datos de criptomonedas estables (stablecoins) utilizando la API CoinGecko. Se exploran datos relacionados con las categorías de criptomonedas, la capitalización de mercado y los precios actuales de las 10 principales criptomonedas estables.

## Requisitos

- Python 3.7+
- Librerías: pandas, seaborn, matplotlib, datetime, time, pycoingecko

## Descripción

El mercado de las criptomonedas ha experimentado un crecimiento exponencial y una creciente adopción a nivel mundial. Este proyecto simula el papel de un Analista de Datos en una empresa financiera que busca comprender mejor el comportamiento y la evolución de las criptomonedas estables. Se utiliza la API CoinGecko para obtener y analizar datos relevantes.

## Pasos Realizados

1. Importar las bibliotecas necesarias: pandas, seaborn, matplotlib, datetime, time y pycoingecko.
2. Establecer conexión con la API CoinGecko.
3. Verificar la disponibilidad de la API mediante `cg.ping()`.
4. Obtener la lista de categorías de monedas utilizando `cg.get_coins_categories_list()`.
5. Filtrar las criptomonedas estables de la lista de categorías.
6. Obtener los datos de capitalización de mercado de las criptomonedas estables en USD.
7. Seleccionar los 10 primeros resultados y crear un DataFrame con la información relevante: nombre, precio actual, capitalización de mercado y suministro circulante.
8. Visualizar la capitalización de mercado de las criptomonedas estables en un gráfico de barras.
9. Visualizar los precios actuales de las criptomonedas estables en otro gráfico de barras.
10. Generar un gráfico circular (pie chart) que muestra la distribución de la capitalización de mercado entre las criptomonedas estables.
11. Calcular y mostrar el porcentaje de la capitalización de mercado de cada criptomoneda estable.

## Resultados

Se obtuvieron los siguientes porcentajes de capitalización de mercado para las criptomonedas estables más importantes:

- Tether: 68.12%
- USD Coin: 21.25%
- Dai: 3.21%
- Binance USD: 2.74%
- TrueUSD: 2.25%
- Frax: 0.66%
- USDD: 0.59%
- Pax Dollar: 0.41%
- PAX Gold: 0.39%
- Tether Gold: 0.38%

## Conclusiones

El análisis permitió visualizar la distribución de la capitalización de mercado entre las criptomonedas estables más importantes. Tether y USD Coin destacan como las criptomonedas estables con mayor capitalización, mientras que otras como Dai y TrueUSD también tienen una participación significativa.

## Uso Adicional

Este proyecto puede servir como punto de partida para un análisis más profundo de las criptomonedas estables, incluyendo investigaciones sobre su adopción, casos de uso y volatilidad en comparación con otras criptomonedas y activos financieros.

## Referencias

- Documentación de CoinGecko API: [CoinGecko API Documentation](https://www.coingecko.com/en/api)

## Autor

Santisteban, Pablo A.
