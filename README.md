# pipeline-ingesta-datos
pipeline-ingesta-datos
Pipeline de Ingesta de Datos
Este pipeline está diseñado para la extracción, transformación y carga (ETL) de datos de riesgo de hipertensión. Consta de las siguientes fases:

Extracción (obtener_datos()):

Lee los datos directamente desde un archivo CSV (riesgo_hipertension_dataset.csv).
Realiza una validación básica para asegurar que el archivo existe.
Retorna un DataFrame de Pandas con los datos.
Carga en Zona RAW (guardar_datos_raw(df)):

Guarda los datos extraídos en una carpeta data/raw/.
Los datos se almacenan sin ninguna transformación, manteniendo su formato original.
Se añade una marca de tiempo al nombre del archivo para mantener un historial.
Pipeline Principal (pipeline_ingesta()):

Orquesta los pasos de extracción y carga RAW.
Registra el inicio y fin del proceso, así como cualquier error que pueda ocurrir.
