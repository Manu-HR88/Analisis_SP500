# INFORME GENERAL

Este informe tiene el objetivo de presentar el trabajo realizado en este proyecto, así como algunas puntos explicativos sobre el tablero de contro realizado.

<br>

## Análisis Exploratorio de Datos

Este etapa se encuentra descrito a detalle en el archivo "EDA_SP500.ipynb"; sin embargo aquí se menciona la estructura de dicho archivo para facilitar la consulta:
* Se utilizó la libraría "yfinance" para extraer los datos históricos del S&P500 y de los ETF's de los sectores.
* Se extrajo información de los balances financieros de las empresas a analizar también de la página [yahoo](https://finance.yahoo.com/).
* Se tomó como periodo a analizar del año 2000 al 2023.
* Se encontraron patrones interesantes y se realizó la investigación correspondiente que a grandes rasgos consta de lo siguiente:

    | Año | Evento |
    | ----------- | ----------- |
    | 2000 | Burbuja tecnológica |
    | 2008 | Crisis mobiliaria |
    | 2011 | Deuda de Grecia y conflicto en Medio Oriente |
    | 2018 | Insertidumbre política y conflicto comercial con China |
    | 2019 | Medidas de la FED para frenar inflación |
    | 2020 | Pandemia COVID-19 |
    | 2021 | Medidas de la FED para frenar inflación
    | 2022 | Guerra Rusia-Ucrania |

* Se identificaron tres sectores cuya correlación con el movimiento del S&P500 es muy notoria (Salud, Tecnológico, Bienes de consumo duradero) y uno en particular que no sigue la tendencia (Energético).
* Se hizo el análisis de estos cuatro sectores a partir de sus Fondos Cotizados en la Bolsa (ETF's).
* Se optó por analizar las empresas que más participación bursátil tienen en cada sector para analizar su salud financiera en el tablero de control.

<br>

## Tablero de control

Este tablero contiene la información gráfica, por lo que es conviente tomar en cuenta los siguientes puntos:

* En la pestaña "Historia" se encuentran los gráficos más importantes del Análisis Exploratorio de Datos.
* En la pestaña "Recomendación" se encuentra el análisis de las empresas a considerar para el análisis de cada una.
* El segmentador de datos que refiere al nombre de las empresas, afectan tanto a las gráficas como a los Indicadores Claves (KPI's).
* Existe un segundo segmentador para el periodo de tiempo que sólo afecta a los Indicadores Claves (KPI's).
* Hay un gráfico con el histórico del precio de la acción de la empresa (uso del filtro), para ver la tendencia y los cambios que ha tenido a lo largo del tiempo.
* La recomendación del día a elegir para invertir está hecho con base en el promedio del valor de cierre de la acción en lo que va del año 2023 para saber el día en que es más bajo el precio a la venta.

### Se consideraron 3 Indicadores Claves:

* Retorno de Inversión: 

    Considera el precio de la acción y la divide entre la utilidad por acción, teniendo como resultado el tiempo aproximado que tomaría al inversionista recuperar su inversión si el comportamiento del precio continúa sin ningún movimiento. 

    El punto objetivo de este indicador es una medida de 8, es decir, que si el tiempo de retorno es mayor a 8 se considera preocupante a medida que crece, pues esto quiere decir que el precio es más elevado que el posible beneficio que se puede obtener.

    Por otro lado, un número negativo tampoco es conveniente puesto indicaría que la empresa no está pagando utilidades e incluso podría ser señal de deuda en general de la empresa.

    <br>

* Rentabilidad de la empresa:

    Este indicador considera la utilidad neta entre los ingresos y el resultado se multiplica por 100 para obtener un porcentaje. Esto indica el márgen de ganancia que está generando por la actividad que desarrolla, es decir, cuánto gana por cada producto que vende o servicio que presta. 

    El punto objetivo es tener un 25% por ciento de ganancia, lo cuál indicaría salud en la forma de producir o prestar el servicio y cobrar por ello.

    Un número negativo podría señalar que cuesta más hacer el producto o prestar el servicio que lo que se cobra.
    
    <br>

* Capacidad de pago:

    Este indicador considera los activos circulantes y los divide entre los pasivos circulantes, para saber qué tan expuesto está para cubrir las deudas a corto plazo con el dinero que se considera tener en el corto plazo también.

    El punto objetivo es tener el valor "1" es decir si se llega a dicho número se considera que se tiene el flujo de efectivo suficiente para pagar las deudas adquiridas al corto plazo.

    Este indicador puede tener números menores a "1" y no considerarse peligroso, aunque sí habría que considerar el caso específico; por otro lado, un número cercano a 2 tampoco es lo ideal, debido a que podría indicar que se tiene capital que no se está trabajando lo que notaría un mal uso de los recursos financieros.

    <br>

## Conclusiones:

* El indicador S&P500 a lo largo de la historia ha sufrido movimientos fuertes tanto al alza como a la baja, pero en general se nota una tendencia alcista desde el 2000. 
* Los sectores que más se correlacionan con el SP500 son la salud, la tecnología y los bienes de consumo duraderos.

        La industria de la salud abarca una amplia gama de áreas, desde la atención médica hasta la farmacéutica. 
        
        Las empresas de tecnología incluyen desde fabricantes de hardware hasta desarrolladores de software y proveedores de servicios en línea. 
        
        Los bienes de consumo duradero son aquellos productos que tienen una vida útil prolongada, como electrodomésticos, muebles y automóviles. Estos productos son considerados esenciales para la vida diaria y, por lo tanto, tienen una demanda constante en la economía.

* El sector energético no sigue la tendencia del SP500 debido a que se ve afectado por factores externos, por ejemplo el precio del petroleo y el gas, los cuales son afectados por factores, como la oferta y la demanda, la producción y los eventos geopolíticos. 

* El sector energético (por sí solo) es capaz de afectar la tendencia del SP500, no se nota tanto por los otros 10 pero en general se puede observar el peso que tiene.

* Las empresas más grandes no necesariamente son las mejores para invertir, pueden existir oportunidades en las empresas de menor tamaño, pero con alto potencial de crecimiento y una buena salud financiera. Además de tomar en cuenta el comportamiento de los precios a través del tiempo.

* No existe ninguna garantía a la hora de invertir, pero se puede tener mayor tranquilidad despúes de analizar no sólo los números sino los proyectos que tenga la empresa y la investigación previa del tema para saber decidir.
