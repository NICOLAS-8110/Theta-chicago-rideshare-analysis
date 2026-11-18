<img width="1280" height="640" alt="WhatsApp Image 2026-11-17 at 3 00 46 PM (7)" src="https://github.com/user-attachments/assets/b2602e00-f52f-4f21-8e65-b7c54f07d90f" />

# 🚖 Θ Proyecto Theta | Análisis de Viajes Compartidos en Chicago (Zuber)

## 📋 Descripción
**Zuber** es una nueva empresa de viajes compartidos que busca expandir su participación en el mercado de transporte urbano de Chicago. Para comprender mejor la dinámica de la movilidad en la ciudad, se analizaron datos históricos combinando consultas SQL sobre bases de datos relacionales y análisis exploratorio de datos (EDA) en Python, evaluando la participación de compañías de taxis, barrios de destino y el impacto de las condiciones meteorológicas.

## 🎯 Objetivos
- ✅ Analizar la participación de las principales compañías de taxis en Chicago.
- ✅ Identificar los barrios con mayor número de viajes finalizados.
- ✅ Comprender los patrones de movilidad urbana de la ciudad.
- ✅ Visualizar los resultados mediante gráficos exploratorios.
- ✅ Evaluar el impacto del clima sobre la duración de los viajes.
- ✅ Aplicar pruebas estadísticas para validar hipótesis de negocio.
- ✅ Generar conclusiones basadas en datos que apoyen la toma de decisiones estratégicas de Zuber.

## 🛠️ Herramientas y Habilidades Utilizadas
* **Bases de datos:** SQL y PostgreSQL
* **Lenguaje:** Python
* **Librerías:** Pandas, NumPy, Matplotlib, Seaborn y SciPy
* **Entorno:** Jupyter Notebook
* **Técnicas:** Consultas SQL avanzadas, Extracción e integración de datos, Análisis Exploratorio de Datos (EDA), Pruebas de hipótesis estadísticas y Visualización de datos.

## 📊 Fuente de Datos y Extracción SQL
El proyecto se desarrolló extrayendo y procesando información desde una base de datos relacional compuesta por las tablas `trips`, `cabs`, `neighborhoods` y `weather_records`:

* **`project_sql_result_01.csv`**: Información sobre compañías de taxis y volumen de viajes (`company_name`, `trips_amount`).
* **`project_sql_result_04.csv`**: Información sobre barrios donde finalizan los recorridos (`dropoff_location_name`, `average_trips`).
* **`project_sql_result_07.csv`**: Registro de viajes entre el Loop y el Aeropuerto Internacional O'Hare (`start_ts`, `weather_conditions`, `duration_seconds`).

## ⚙️ Metodología
1. **Extracción con SQL:** Ejecución de consultas para identificar compañías líderes, calcular promedios de finalización por barrio e integrar registros meteorológicos con tiempos de viaje.
2. **Preparación de datos:** Importación de archivos CSV, revisión de tipos, verificación de consistencia y depuración de variables.
3. **Análisis exploratorio:** Estudio de la actividad por compañía de taxi y cartografía de movilidad urbana según los destinos más frecuentes.
4. **Prueba de hipótesis:** Evaluación estadística para determinar si la duración de los trayectos entre el Loop y O'Hare varía significativamente en días lluviosos frente a climas favorables.

## 💡 Principales Hallazgos
* **Concentración de mercado:** *Flash Cab* se posicionó como la compañía con mayor volumen de viajes, evidenciando un mercado concentrado en pocas empresas líderes y una disminución gradual en la actividad de los competidores secundarios.
* **Zonas de alta demanda:** *Loop* lidera destacándose como el principal centro económico, comercial y turístico de Chicago (superando los 10,000 viajes analizados), seguido de cerca por *River North*.
* **Impacto del clima en los trayectos:** La prueba estadística confirmó que las condiciones meteorológicas afectan de manera directa la movilidad.

## 🧪 Resultados de la Prueba de Hipótesis
* **Hipótesis nula (H₀):** La duración promedio de los viajes desde el Loop hasta el Aeropuerto O'Hare es la misma durante los sábados lluviosos y los de clima favorable.
* **Hipótesis alternativa (H₁):** La duración promedio de los viajes es diferente bajo ambas condiciones climáticas.
* **Nivel de significancia ($\alpha$):** `0.05`
* **Resultado:** `p-value = 6.518 × 10⁻¹²` (`0.0000000000065...`)
* **Conclusión:** Dado que `p-value < α`, **se rechaza la hipótesis nula**. Existe evidencia estadística concluyente de que la lluvia incrementa la congestión, reduce la velocidad de circulación y altera significativamente la duración de los viajes hacia el aeropuerto.

## 📈 Visualizaciones Desarrolladas
* Gráfico de barras de viajes por compañía de taxis (evidenciando el liderazgo de *Flash Cab*).
* Top 10 de barrios con mayor número de finalizaciones de recorridos (destacando *Loop* y *River North*).
* Gráficos comparativos de distribución de tiempos de viaje bajo diferentes escenarios climáticos.

## 📂 Archivos Principales
* `Proyecto_Theta___Análisis_de_Viajes_Compartidos_en_Chicago.ipynb`
* `moved_project_sql_result_01.csv`
* `moved_project_sql_result_04.csv`
* `moved_project_sql_result_07.csv`

## 🏁 Conclusión
El análisis integral mediante SQL y Python permitió a Zuber descifrar las dinámicas críticas del transporte urbano en Chicago. La alta concentración de viajes en actores clave como *Flash Cab*, la centralidad indiscutible de zonas como el *Loop* y la fuerte afectación del clima en rutas estratégicas como el trayecto al Aeropuerto O'Hare (validado estadísticamente) ofrecen una ventaja operativa invaluable. Estos hallazgos proporcionan bases sólidas para anticipar cambios en la demanda, optimizar la asignación de recursos y fortalecer la estrategia competitiva de Zuber en el mercado.
