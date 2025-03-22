# Debt-Collection
Machine Learning Model - Debt Collection

## Descripción del Caso

La empresa en cuestión ofrece servicios de Call Center especializados en diversas áreas, incluyendo gestión de ventas, cross-selling, comunicaciones generales, retención de clientes y cobranzas. El principal indicador de rendimiento (KPI) es la **contactabilidad de los leads**, definida como:

$$
Contactabilidad = \frac{CE}{CE + CNE}
$$

Donde:
- **CE**: Contacto Efectivo
- **CNE**: Contacto No Efectivo

Recientemente, la empresa ha experimentado una disminución en el ratio de contactabilidad, pasando de un promedio del **34%** a solo un **30%**. Este descenso ha impactado negativamente en la capacidad de la empresa para recuperar montos adeudados, lo que representa un desafío significativo en la gestión de cobranzas.

## Problema Principal

¿Cómo puede la empresa mejorar la contactabilidad en la gestión de cobranzas para diferentes campañas, asegurando así una mayor efectividad y recuperación de deuda?

## Base de Datos

La base de datos proporcionada contiene información detallada sobre los clientes y las gestiones realizadas. A continuación, se describen las variables clave:

| Variable       | Descripción                                                                 |
|----------------|-----------------------------------------------------------------------------|
| MES            | Mes de observación o periodo de ejecución.                                  |
| CLIENTE        | Identificador del cliente o prospecto.                                      |
| NRO_VEC_COB    | Número de veces que el cliente cayó en cobranzas.                           |
| PDPs_ROTAS     | Número de promesas que el cliente hizo sin cumplir.                         |
| ESTADO_PDP     | Estado de promesa de pago. {0: Sin promesa; 1: Con promesa temprana; 2: Con promesa tardía; 3: Con promesa rota.} |
| NRO_CUOTAS     | Número de cuotas adeudadas.                                                 |
| MES_0          | Deuda vencida actual.                                                       |
| MES_1          | Deuda vencida del mes anterior.                                             |
| MES_2          | Deuda vencida hace dos meses.                                               |
| FECHALLAMADA   | Fecha de la gestión del lead o cliente.                                     |
| HORA           | Hora de la gestión del lead o cliente.                                      |
| DEUDA_TOTAL    | Deuda total al cierre del mes.                                              |
| ESTATUS        | BT= Titulares, OTROS= No titulares                                          |
| ACTIVACION     | Año de activación como cliente.                                             |
| MORA           | Estado de mora. {1: Normal; 0: Deficiente}                                  |
| TIPOCONTACTO   | Estado resultante de la llamada. {COEF: Contacto efectivo; CNE: Contacto No efectivo} |

## Objetivo del Estudio

El objetivo principal de este estudio es desarrollar un modelo que permita mejorar la contactabilidad en la gestión de cobranzas. Para ello, se analizarán los datos disponibles con el fin de identificar patrones y factores que influyen en la efectividad de los contactos. El modelo resultante deberá proporcionar recomendaciones estratégicas para optimizar las campañas de cobranza y aumentar el ratio de contactabilidad.

## Estructura del Repositorio

- **data/**: Contiene los archivos de datos utilizados en el análisis.
- **notebooks/**: Incluye los cuadernos de Jupyter con el análisis exploratorio y el desarrollo del modelo.
- **txt/**: Archivo .txt para la instalacion de las librerias empleadas.
- **README.md**: Este archivo, que proporciona una descripción general del proyecto.

## Requisitos

Para ejecutar los scripts y cuadernos de este repositorio, se necesitan las siguientes librerías de Python:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- lightgbm

Puedes instalar las dependencias utilizando el siguiente comando:

```bash
pip install -r requirements.txt
