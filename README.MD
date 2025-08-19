# 📊 Análisis Comparativo de Tiendas - Challenge Data Science

## 🧠 Objetivo

Analizar el desempeño comercial de cuatro tiendas digitales para identificar oportunidades de mejora y tomar decisiones estratégicas. El objetivo final fue recomendar si alguna tienda debía ser cerrada o transformada, en función de métricas de rentabilidad, satisfacción y comportamiento de ventas.

---

## ✅ Conclusión General

> **Se recomienda vender o cerrar la Tienda 4 y enfocar recursos en fortalecer las Tiendas 1, 2 y 3**, que muestran un mejor balance entre facturación, rentabilidad y satisfacción del cliente.

---

## 📌 Justificación

- **Menor ingreso total y por artículo.**
- **Ganancia neta más baja**, incluso con el costo de envío más económico.
- **Satisfacción aceptable, pero no sobresaliente.**
- **Desempeño inconsistente** en productos más vendidos.
- Las **visualizaciones respaldan consistentemente** su bajo rendimiento general.

---

## 📥 Importación y Preparación de Datos

Se cargaron las bases de datos de cada tienda directamente desde GitHub mediante `pandas`. Luego, se integraron en un solo diccionario para facilitar el análisis comparativo.

```python
import pandas as pd

urls = {
    "Tienda 1": "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_1%20.csv",
    "Tienda 2": "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_2.csv",
    "Tienda 3": "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_3.csv",
    "Tienda 4": "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_4.csv"
}

tiendas = {nombre: pd.read_csv(url) for nombre, url in urls.items()}
