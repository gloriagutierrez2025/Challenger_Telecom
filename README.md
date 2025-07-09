**Challenger_Telecom**

**Introducción**

El análisis se enfoco en comprender que factores están influyendo en la cancelación de clientes de TelecomX.
A partir de un conjunto de datos historicos se identificó variables relacionadas a la cancelación de servicios de Telecom, utilizando análisis estadísticos y visuales. Se identificaron patrones claros de comportamientos, lo que permitió definir acciones concretas para reducir el porcentaje Churn (cancelación).

**Tecnologías**

- Notebook electronico Google Colab con Python

- Librerías:Pandas,Matplotlip,Seaborn,Numpy,requests,json.

**Limpieza y tratamiento de Datos**

Importación de datos desde Github, utilizando la biblioteca requests.

Normalización del archivo json, se usó pd.json_normalize(),para convertir la estructura anidada del json en un DataFrame plano de pandas, con el fin de poder trabajar con el archivo como una tabla.

Se hizo limpieza en nombres de las columnas, reemplazando los puntos por guíon bajo para facilitar el acceso a las columnas.

Reemplazo de valores vaciós por Nan que es el formato estandar por pandas para valores faltantes y se eliminó duplicados para evitar distorsiones en los análisis.

Filtrado de registros invalidos, se eliminaron los valores que no tenian registros validos en la columna churn (Cancelación),conservando solo valores Yes y No.

Conversión de columnas númericas, se forzó la conversión de algunas columnas claves como Charges_Monthly a tipo númerico, manejando errores con Nan.

Codificación de variables binarias Yes/No a 1/0.

Renombramiento de columnas claves a español

**Análisis exploratorio de datos**

Creación de columna gasto mensual/diario, a través de columna cuentas diarias para explorar el gasto promedio diario y mensual por cliente.
Para poder encontrar las variables con mayor impacto en la cancelación, se creó gráficos correlacionados con variable Churn (Cancelación), como Género, tiempo de contrato, distribución de gastos totales,  cancelación por método de pago y por tipo de contrato. Proporción de clientes que cancelan versus quienes no cancelan.

Gráfico con proporción de clientes que cancelan verus quienes no cancelan servicios

<img width="407" height="435" alt="Image" src="https://github.com/user-attachments/assets/7fc0fd27-eea9-4779-b94c-7af508d57bcd" />

Gráfico 

<img width="590" height="390" alt="Image" src="https://github.com/user-attachments/assets/bf343f70-882f-4d99-843c-04f94668c576" />

Gráfico

<img width="785" height="390" alt="Image" src="https://github.com/user-attachments/assets/1003e1c0-54b5-41dc-ba39-65ac0ece9dae" />

**Las variables con mayor impacto en la cancelación de servicios son:**

- Tipo de Contrato

- Tiempo de Contrato

- Gastos Mensuales

- Método de pago

- Servicios Contratados

**Conclusiones**

De acuerdo con la información recopilada podemos ver que clientes que optan por contrato mensual suelen cancelar más en comparación con quienes optan por contrato anual. Asi mismo quienes llevan poco tiempo de contrato muestran una tendencia a cancelar más sus servicios.
Otros factores influyentes en las cancelaciones son los gastos mensuales altos y el método de pago como "Electronic Check", ambos muestran una tasa más alta de cancelación en comparación con el resto de las variables evaluadas.

**Recomendaciones**

- Incentivar contratos anuales

- Ofrecer beneficios por permanencia

- Ofrecer algun regalo para clientes con alta tarifa

- Seguimiento a nuevos clientes





