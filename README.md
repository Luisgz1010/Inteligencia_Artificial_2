# Predicción de precios de vivienda

Este proyecto compara una **Regresión Lineal** y un **Árbol de Decisión** para estimar el precio de una vivienda usando el dataset [Housing Prices Dataset de Kaggle](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset).

## Abrir en Google Colab

1. Descargue `outputs/modelo_precios_vivienda_colab.ipynb`.
2. Súbalo a [Google Colab](https://colab.research.google.com/) o ábralo desde un repositorio de GitHub.
3. Ejecute las celdas en orden. El cuaderno descarga `Housing.csv` desde la fuente pública de Kaggle.

## Qué contiene

- Verificación inicial de estructura, tipos y datos faltantes.
- Preparación automática de atributos numéricos y categóricos.
- Entrenamiento reproducible de Regresión Lineal y Árbol de Decisión.
- Comparación mediante R², MAE y RMSE tanto en entrenamiento como en prueba.
- Gráficas de desempeño y predicción frente a valor real.
- Conclusión generada a partir de las métricas obtenidas al ejecutar el cuaderno.

## Publicar en GitHub

Después de crear un repositorio vacío en GitHub, ejecute en una terminal dentro de esta carpeta:

```powershell
git init
git add outputs/README.md outputs/modelo_precios_vivienda_colab.ipynb
git commit -m "Modelo de predicción de precios de vivienda"
git branch -M main
git remote add origin https://github.com/USUARIO/NOMBRE-DEL-REPOSITORIO.git
git push -u origin main
```

No se versionan datos descargados: el cuaderno los obtiene al ejecutarse, para respetar la fuente original y mantener el repositorio liviano.
