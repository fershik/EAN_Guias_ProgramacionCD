**TRABAJO GUIA 2**

**Integrantes del Trabajo:**  John Alexander Castañeda Gordillo y Deisy Fernanda Camacho Vargas

**Instrucciones de ejecución**
1. Descargar el archivo Guia_2_Solución.ipynb
2. Descargar el dataset telecom_churn.csv
3. Abrir archivo Guia_2_Solución.ipynb en google colab
4. Cargar dataset en google colab en la opcion Archivos (Subir Archivo)
5. Ejecutar las celdas de código.

**Objetivo**  
Por medio de lenguaje Python usando la libreria Pandas se desarrolla cada una de las siguientes partes de la guia:

- **Exploración y Limpieza de Datos**
  En esta sección mportamos la libreria pandas, cargamos el dataset en un dataframe de pandas llamado *df* usando la funcion read.csv() y lo visualizamos con la funcion head().
  Tambien verificamos el tamaño del dataframe usando la funcion shape() y vemos la información general de dataframe con la funcion info().
  Finalmente verificamos si existen valores nulos en alguna de las columnas del dataframe con la funcion isnull()
  
- **Análisis de Churn y Factores Relacionados**
  En esta sección calculamos el porcentaje de clientes desertados creando un dataframe nuevo llamado *clientes_churn* en donde le asignamos todos los clientes con valor 1 en la columna *chrum*, teniendo la cantidad de clientes con el churn calculamos el porcentaje diviviendo este por el total del clientes.
  Tambien identificamos si los clientes con plan internacional tienen mayor tasa de deserción. En este punto calculamos el porcentaje de desertados que tenian el plan internacional y el porcentaje de desertados sin el plan internacionacional y los comparamos.
  El mismo ejercicio se realizo con los clientes con buzon de voz.
    
- **Análisis de la Duración del Servicio y Deserción**
  Teniendo ya previamente nuestro dataframe con los clientes desertados (*clientes_churn*) se hace calculo del promedio de la cuenta (account length) con la funcion mean().
  Tambien se crea el dataframe de los clientes no desertados (*clientes_no_churn*) y se calculo el promedio de la cuenta de éstos usando la misma función.
   
- **Relación entre Deserción y Uso del Servicio**
  Aqui calculamos el *total day minutes* para los desertados y no desertados aplicando la funcion sum() en la columna *total day minutes* para los dataframes *clientes_churn* y *clientes_no_churn*
  El mismo ejercicio se realiza para las columnas *total night minutes* y *total day calls*
  Los valores totales se comparan para comparar la cantidad de minutos para los desertados y no desertados

- **Impacto de las Llamadas al Servicio al Cliente en la Deserción**
  En esta seccion se calcula primeramente el promedio de la columna *customer service calls* con la funcion mean()
  Luego creamos los dos grupos de clientes con las indicaciones en el ejercicio (clientes que llamaron más de 3 veces al servicio al cliente y clientes que llamaron 3 veces o menos)
  Teniendo los dos grupos se calcula su correspondiente tasa de churn contando los clientes de cada grupo con la columna churn = 1 y diviendolos por el total de clientes del grupo.
  Al final se comparar los resultados de las tasas de ambos grupos.
  
- **Análisis del Costo de las Llamadas y Churn**
  Finalmente en esta última sección calculamos el costo total del *total day charge* y *total night charge* con la funcion sum() aplicados para los dataframes *clientes_churn* y *clientes_no_churn*
  En ambos indicadores realizamos la comparación de los valores. 
