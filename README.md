# Análisis de Tarifas de Megaline

Este proyecto tiene como objetivo analizar los ingresos generados por dos planes tarifarios diferentes de Megaline, una empresa de telecomunicaciones. Se analizaron datos de 500 clientes de Megaline durante el año 2018 para determinar cuál de las tarifas, Surf o Ultimate, es más rentable para la empresa.

## Índice

1. [Introducción](#intro)
2. [Descripción de las Tarifas](#tarifas)
3. [Diccionario de Datos](#data-dictionary)
4. [Resumen del Proyecto](#project-summary)
5. [Principales Análisis Realizados](#key-analyses)
6. [Conclusiones Generales](#conclusions)
7. [Recomendaciones](#recommendations)
8. [Acceso a los Datos](#data-access)

## Introducción <a id='intro'></a>

En este proyecto, trabajamos como analista para Megaline, un operador de telecomunicaciones que ofrece dos tarifas de prepago a sus clientes: Surf y Ultimate. El objetivo principal del análisis es determinar cuál de las dos tarifas genera más ingresos para la empresa, proporcionando información valiosa al departamento comercial para ajustar el presupuesto de publicidad de manera eficiente.

Para llevar a cabo este análisis, utilizamos datos de 500 clientes de Megaline, recopilados durante el año 2018. Los datos incluyen información sobre los clientes, las tarifas que utilizan, la cantidad de llamadas realizadas, los mensajes de texto enviados y el uso de datos. Analizaremos el comportamiento de los clientes y compararemos los ingresos generados por cada tarifa mediante pruebas estadísticas.

## Descripción de las Tarifas <a id='tarifas'></a>

### Tarifa Surf
- Pago mensual: $20
- 500 minutos al mes, 50 SMS y 15 GB de datos
- Cargos adicionales:
  - 1 minuto: $0.03
  - 1 SMS: $0.03
  - 1 GB de datos: $10

### Tarifa Ultimate
- Pago mensual: $70
- 3000 minutos al mes, 1000 SMS y 30 GB de datos
- Cargos adicionales:
  - 1 minuto: $0.01
  - 1 SMS: $0.01
  - 1 GB de datos: $7

## Diccionario de Datos <a id='data-dictionary'></a>

### Tabla `users` (datos sobre los usuarios):
- `user_id`: identificador único del usuario
- `first_name`: nombre del usuario
- `last_name`: apellido del usuario
- `age`: edad del usuario (en años)
- `reg_date`: fecha de suscripción (dd-mm-aa)
- `churn_date`: fecha en la que el usuario dejó de usar el servicio (si el valor es ausente, la tarifa se estaba usando cuando fue extraída esta base de datos)
- `city`: ciudad de residencia del usuario
- `plan`: nombre de la tarifa

### Tabla `calls` (datos sobre las llamadas):
- `id`: identificador único de la llamada
- `call_date`: fecha de la llamada
- `duration`: duración de la llamada (en minutos)
- `user_id`: identificador del usuario que realiza la llamada

### Tabla `messages` (datos sobre los SMS):
- `id`: identificador único del SMS
- `message_date`: fecha del SMS
- `user_id`: identificador del usuario que manda el SMS

### Tabla `internet` (datos sobre las sesiones web):
- `id`: identificador único de la sesión
- `mb_used`: volumen de datos gastados durante la sesión (en megabytes)
- `session_date`: fecha de la sesión web
- `user_id`: identificador del usuario

### Tabla `plans` (datos sobre las tarifas):
- `plan_name`: nombre de la tarifa
- `usd_monthly_fee`: pago mensual en dólares estadounidenses
- `minutes_included`: minutos incluidos al mes
- `messages_included`: SMS incluidos al mes
- `mb_per_month_included`: datos incluidos al mes (en megabytes)
- `usd_per_minute`: precio por minuto tras exceder los límites del paquete
- `usd_per_message`: precio por SMS tras exceder los límites del paquete
- `usd_per_gb`: precio por gigabyte de los datos extra tras exceder los límites del paquete (1 GB = 1024 megabytes)

## Resumen del Proyecto <a id='project-summary'></a>

En este proyecto, analizamos y evaluamos diversos aspectos del uso de los servicios de telecomunicaciones por parte de los usuarios de diferentes planes tarifarios de Megaline. Se utilizaron datos de seis tablas para llevar a cabo un análisis exhaustivo y llegar a conclusiones significativas sobre el comportamiento y los ingresos generados por los usuarios de los planes Surf y Ultimate.

## Principales Análisis Realizados <a id='key-analyses'></a>

1. **Comparación de la Duración Promedio de Llamadas por Plan**:
   - Se comparó la duración promedio de las llamadas realizadas por los usuarios de los planes "Ultimate" y "Surf" mediante un gráfico de barras.
   - **Conclusión**: No se encontraron diferencias significativas en la duración promedio de las llamadas entre los dos planes.

2. **Análisis del Número de Minutos Mensuales Utilizados**:
   - Se visualizó la distribución del número de minutos de llamadas mensuales por plan mediante un histograma.
   - **Conclusión**: La distribución de los minutos utilizados muestra que los usuarios de ambos planes tienen comportamientos de uso distintos.

3. **Evaluación del Ingreso Promedio por Plan**:
   - Se realizó una prueba t de dos muestras independientes para comparar los ingresos promedios mensuales generados por los usuarios de los planes "Ultimate" y "Surf".
   - **Conclusión**: Se encontró una diferencia significativa entre los ingresos promedios de los dos planes, con los usuarios del plan "Ultimate" generando ingresos significativamente mayores.

4. **Análisis Regional del Ingreso Promedio**:
   - Se evaluó si el ingreso promedio de los usuarios en el área de Nueva York y Nueva Jersey (NY-NJ) es diferente al de los usuarios de otras regiones.
   - **Conclusión**: No se encontró una diferencia significativa entre los ingresos promedios de los usuarios en NY-NJ y los de otras regiones.

## Conclusiones Generales <a id='conclusions'></a>

- **Diferencias en Ingresos por Plan**: Los usuarios del plan "Surf" generan ingresos significativamente mayores en comparación con los usuarios del plan "Ultimate". Esto puede deberse a diferencias en las tarifas, beneficios incluidos en cada plan, patrones de uso, o mayor número de usuarios en el plan "Surf".
- **Impacto Regional Insignificante**: La ubicación geográfica de los usuarios, específicamente si están en el área de NY-NJ o en otras regiones, no parece tener un impacto significativo en los ingresos promedios generados por los usuarios. Esto indica que los planes tarifarios y los patrones de uso son consistentes en diferentes regiones.

## Recomendaciones <a id='recommendations'></a>

- **Revisión de Tarifas y Beneficios**: Considerar la revisión de las tarifas y beneficios incluidos en los planes para optimizar los ingresos y atraer a más usuarios a planes más rentables.

## Acceso a los Datos <a id='data-access'></a>

Los archivos CSV utilizados en este análisis están disponibles para su consulta y descarga en el siguiente enlace de Google Drive:

[Enlace a los datos en Google Drive](https://drive.google.com/drive/folders/1ADjA-KTxO-yuXARr9mqHhvj3G4sjUUVW?usp=sharing)

