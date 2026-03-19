# 📊 Marketing Analytics – LTV, CAC & User Behavior Analysis

Este proyecto analiza el comportamiento de usuarios y el rendimiento de las inversiones en marketing para una empresa de venta de entradas de eventos.

El objetivo es comprender cómo los usuarios interactúan con la plataforma, evaluar la rentabilidad de los canales de adquisición y determinar cuándo los ingresos cubren el costo de adquisición de clientes.

## 🎯 Objetivos 

- Analizar el comportamiento de los usuarios (visitas, sesiones y retención)
- Evaluar el proceso de conversión de usuarios a clientes
- Calcular métricas clave como LTV (Lifetime Value), CAC (Customer Acquisition Cost) y ROMI
- Identificar las fuentes de marketing más rentables
- Proponer recomendaciones para optimizar la inversión en marketing

## 📂 Dataset

El análisis se basa en tres conjuntos de datos:

### Visitas
- Uid (usuario)
- Device (dispositivo)
- Start Ts / End Ts (sesión)
- Source Id (fuente de adquisición)

### Órdenes
- Uid
- Buy Ts (fecha de compra)
- Revenue (ingresos)

### Costos
- source_id
- dt (fecha)
- costs (gasto en marketing)

## 🛠️ Herramientas y Tecnologías

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Jupyter Notebook

## 📊 Metodología

### 1. Preparación de datos
- Limpieza y validación
- Conversión de tipos de datos
- Identificación de usuarios únicos

### 2. Análisis de comportamiento
- Usuarios activos diarios, semanales y mensuales
- Número de sesiones por usuario
- Duración de sesiones
- Retención de usuarios

### 3. Análisis de ventas
- Tiempo hasta la primera compra (cohortes)
- Número de pedidos por usuario
- Valor promedio de compra
- Ingresos por usuario (LTV)

### 4. Análisis de marketing
- Gasto total y por fuente
- Costo de adquisición de clientes (CAC)
- Retorno de la inversión (ROMI)

## 🔍 Resultados e Insights

- Observé que el tráfico y recurrencia de visitantes al portal web es coherente con el tipo de negocio. La métrica más importante para este análisis no es la recurrencia en la página sino la tasa de conversión. 
- Al analizar las ventas me di cuenta que la tendencia de los usuarios es la compra impulsiva (el mismo día del registro). El comportamiento más habitual no se explica por las medidas de tendencia central (media 17 días) o de dispersión (std 46 días). Al menos el 50% de los casos compran el día del registro. Un 25% compran durante los sigueintes 2 días y el 25% restante compran en los siguientes meses.
- A pesar de ser los clientes impulsivos los que representan mayores ingresos para la compañía, son los usuarios con compra planificada los que a largo plazo aportan mayor valor. Para ellos, se podrían implementar estrategias de marketing que les favorezcan y de esta forma estimular sus compras.
- En cuanto al análisis de marketing, observamos que no todas las fuentes representaron ganancias para la compañía, de hecho, la fuente 3 la cual fue la más costosa siempre presentó ROMI negativo. La fuente #1 siempre se mantuvo en un umbral positivo y en promedio representa el retorno más valioso.
