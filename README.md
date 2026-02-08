# 📊Sesgo de la Volatilidad

Volumen vs. Movimientos Extremos de Precio

## 🧠Descripción del Proyecto

Este proyecto analiza la relación entre movimientos extremos de precio y picos anómalos de volumen, con el objetivo de detectar episodios de pánico o euforia en el mercado.

La hipótesis central es que los movimientos diarios significativos (subas o caídas fuertes) suelen venir acompañados de un aumento desproporcionado del volumen negociado, reflejando reacciones emocionales o decisiones forzadas de los participantes del mercado.

## 🎯Objetivo

Identificar acciones en las que:
- El precio se mueve más de ±3% intradía
- El volumen negociado es más del doble del promedio de los últimos 30 días
- Esto permite detectar activos donde el mercado está reaccionando de forma no lineal ante la información disponible.

## 🔍 Pregunta de Investigación (Insight)

- ¿Qué acciones presentan picos de volumen significativos específicamente en los días con movimientos extremos de precio, indicando pánico o euforia?

## 🧮Metodología

- Se calcula el cambio porcentual absoluto intradía entre apertura y cierre.
- Se estima el volumen promedio de los últimos 30 días para cada acción.

Se filtran únicamente los días donde:
- El movimiento de precio supera el 3%
- El volumen es superior a 2× el promedio histórico reciente

Los resultados se ordenan priorizando:
- Eventos más recientes
- Movimientos de precio más extremos

## 📈Métricas Clave

- Cambio diario absoluto (%)
- Volumen diario
- Volumen promedio 30 días
- Relación volumen actual vs. histórico

## 💡Valor de Negocio

- Detecta eventos de estrés o euforia en tiempo real

Útil para:
- Confirmar rupturas (breakouts)
- Detectar capitulación del mercado
- Filtrar señales falsas en estrategias de momentum
- Aporta contexto emocional al análisis técnico tradicional

## 🛠️Requisitos Técnicos

Base de datos con:
- precios_diarios (open, close, volume, fecha)

Soporte para:
- Subconsultas
- Funciones de fecha (DATEADD)
- Compatible con SQL Server / T-SQL

## 🚀Casos de Uso

- Trading de volatilidad
- Estrategias contrarian (fade de pánico)
- Confirmación de noticias implícitas en precio y volumen
- Análisis de comportamiento del mercado

## 📌 Nota Final

- Este análisis no evalúa dirección, sino intensidad emocional del mercado.
- Un pico de volumen con un gran movimiento no dice qué hacer, pero sí indica cuándo el mercado está gritando.

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
