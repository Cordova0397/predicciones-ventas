# Proyecto de Predicción de Ventas

## Introducción
El objetivo de este proyecto es ayudar a un minorista a comprender las propiedades de los productos y puntos de venta que juegan un papel crucial en el aumento de las ventas. Para ello, se desarrollaron y mejoraron varios modelos de predicción de ventas.

## Descripción de los Datos
El conjunto de datos contiene información sobre varios productos vendidos en diferentes puntos de venta. Las principales columnas incluyen:

- `Item_Identifier`: Identificador único del producto.
- `Item_Weight`: Peso del producto.
- `Item_Fat_Content`: Contenido de grasa del producto.
- `Item_Visibility`: Visibilidad del producto.
- `Item_Type`: Tipo de producto.
- `Item_MRP`: Precio de venta del producto.
- `Outlet_Identifier`: Identificador único del punto de venta.
- `Outlet_Establishment_Year`: Año de establecimiento del punto de venta.
- `Outlet_Size`: Tamaño del punto de venta.
- `Outlet_Location_Type`: Tipo de ubicación del punto de venta.
- `Outlet_Type`: Tipo de punto de venta.
- `Item_Outlet_Sales`: Ventas del producto en el punto de venta.

## Análisis Exploratorio de Datos (EDA)
Se realizaron varios pasos de EDA para limpiar y entender mejor los datos:

1. **Manejo de Valores Nulos**: 
   - Los valores nulos en `Item_Weight` fueron imputados usando la media de pesos por `Item_Identifier`.
   - Los valores nulos en `Outlet_Size` fueron imputados como 'Small' basados en el análisis de `Outlet_Location_Type`.

2. **Visualizaciones**:
   - **Distribución de ventas:**
     ![Distribución de Ventas](path_to_image1.png)
     Este gráfico muestra la distribución de las ventas de productos en los diferentes puntos de venta.
   - **Ventas por tipo de producto:**
     ![Ventas por Tipo de Producto](path_to_image2.png)
     Este gráfico muestra las ventas medias por tipo de producto.
   - **Ventas por tamaño del punto de venta:**
     ![Ventas por Tamaño del Punto de Venta](path_to_image3.png)
     Este gráfico muestra las ventas por tamaño del punto de venta.
   - **Ventas vs Precio del producto:**
     ![Ventas vs Precio del Producto](path_to_image4.png)
     Este gráfico muestra la relación entre las ventas y el precio del producto.
   - **Ventas totales por tipo de punto de venta:**
     ![Ventas Totales por Tipo de Punto de Venta](path_to_image5.png)
     Este gráfico muestra las ventas totales por tipo de punto de venta.

## Preprocesamiento de Datos
- Las columnas categóricas fueron transformadas usando `OneHotEncoder`.
- Los datos fueron normalizados utilizando `StandardScaler`.

## Modelos de Regresión
Se probaron varios modelos para predecir las ventas:

### K-Nearest Neighbors (KNN)
Resultados:
Error cuadrático medio (MSE): 1666974.360790399
Coeficiente de determinación (R^2): 0.4216665767872708

## Regresion Lineal
Resultados:

MAE: 827.6673742946364
MSE: 1261327.7976484802
RMSE: 1123.0885083770024
R^2: 0.5624

## Bosques Aleatorios
Resultados:
R^2: 0.5508170421288534
MSE: 1294714.1633859728
RMSE: 1137.8550713451923

## Resultados y Recomendaciones
KNN: R^2: 0.4217, MSE: 1666974.36, RMSE: 1292.68
Regresión Lineal: R^2: 0.5624, MAE: 827.67, MSE: 1261327.80, RMSE: 1123.09
Bosques Aleatorios: R^2: 0.5508, MSE: 1294714.16, RMSE: 1137.86
Los bosques aleatorios proporcionaron el mejor rendimiento en términos de R^2 y RMSE. Se recomienda seguir optimizando este modelo y explorar más características.

## Conclusiones
Este proyecto demuestra cómo diferentes modelos de regresión pueden ser utilizados para predecir ventas. Los bosques aleatorios mostraron ser el modelo más efectivo. Se sugiere seguir mejorando este modelo y considerar más características para aumentar la precisión de las predicciones.

## Repositorio
Este proyecto está disponible en GitHub. El repositorio incluye:

Código fuente
Datos utilizados
Resultados de los modelos
Diapositivas de la presentación
Grabación de la presentación

## Autor
Carlos Eloy Cordova Sandoval

Este README proporciona una descripción general del proyecto, detalles sobre el análisis de datos, modelos utilizados, resultados, y recomendaciones para mejorar. También incluye información sobre la organización del repositorio.
