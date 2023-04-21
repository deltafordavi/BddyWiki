# Azure de Microsoft

## Data Factory

Definición según los [Documentos de Microsoft][r1] 

>*Se trata de un servicio de integración de datos y ETL basado en la nube que le permite crear flujos de trabajo orientados a datos a fin de coordinar el movimiento y la transformación de datos a escala*

Los components principales que Data Factory puede contener o dar servicio son: 

>  -  Pipelines
>  -  Actividades
>  -  Conjuntos de datos
>  -  Servicios vinculados
>  -  Flujos de datos
>  -  Integration Runtime



### Notas al [Documento de Microsoft][r1] 

#### Contexto de uso del Data Factory

>*Los macrodatos requieren un servicio que pueda orquestar y operacionalizar los procesos para convertir estos enormes almacenes de datos sin procesar en información empresarial en función de la cual se puedan emprender acciones*



#### Ejemplos de uso de Data Factory


¿Quién y el qué?
>*empresa de juegos que recopila petabytes de registros de juegos generados por juegos en la nube. La empresa quiere analizar estos registros para obtener información sobre las preferencias de los clientes, los datos demográficos y el comportamiento de uso. [...]  la empresa debe usar datos de referencia. [...]*



¿Cómo y desde dónde?
>*La empresa quiere usar estos datos del almacén de datos local y combinarlos con datos de registro adicionales que tiene en un almacén de datos en la nube.*


#### Potencial de Acción

- Crear y schedule Flujos de trabajo y datps
- Ingestión de Información/datos desde La Nube y entornos Locales
- ETL y ELT de alta complejidad
- Acceso a servicios de (pre y post)Proceso como:
  -  Azure HDInsight Hadoop 
  -  Azure Databricks y 
  -  Azure SQL Database.
- Acceso a almacenes de Datos como
    - Azure Synapse Analytics
  
- Conexión y recopilación de datos de distintas 
  - fuentes (SQL vs no SQL vs Texto llano vs "código")
  
  en distintos 

  - entornos    (local vs nube vs web vs SaaS vs FTP server vs Muchos More)
  con diferentes
  - Ritmos de entrada y salidas
  
- Transformación y enriquecimiento analítico
- Desarrollo y Distribución incremental de :
  - Procesos ETL
  - Procesos ELT
- Cargado de datos en productos de almacenamiento como
  -  Azure Data Warehouse
  -  Azure SQL Database
  -  Azure Cosmos DB
- Supervisión de alto nivel haciendo uso de
    -  Azure Monitor
    -  API
    -  PowerShell
    -  Registros de Azure Monitor y 
    -  Paneles de mantenimiento de Azure Portal

#### Acciones (y efectos) en sí

- Usar [Actividad de Copia][r4]
- Recopilar datos  de
  - Azure Data Lake Storage ó
  - Azure Blob Storage 
- Transformarlos con un proceso a través de

  -  Azure Data Lake Analytics ó
  - clúster de Azure HDInsight Hadoop
  - Clústeres de Spark 
  - ML
- Conexiones a de Azure DevOps y gitHub (CI/CD)
  

## Terminología 

Términos y sus prespcriptivas definiciones que lo hasen todo guay

### General

 **Pipeline**
 
 **PaaS** De la Voz Inglesa *Plaftorm as a service*



**CI/CD** *Continuous ingestion slash Continous delivery*

### Azure

**Actividades**
 *Las actividades representan un paso del procesamiento en una canalización. Por ejemplo, puede usar una actividad de copia para copiar datos de un almacén de datos a otro*
 
 **Conjuntos de datos** 
 > *Os conjuntos de datos representan las estructuras de datos de los almacenes de datos que simplemente apuntan o hacen referencia a los datos que desea utilizar en sus actividades como entradas o salidas.*

 **Servicios vinculados**
 > *un servicio vinculado define la conexión al origen de datos y un conjunto de datos representa la estructura de los datos* [...] *Los servicios vinculados se utilizan con dos fines en Data Factory:*
 >> - *Para representar un almacén de datos que incluye, entre otros, una base de datos de SQL Server, una base de datos de Oracle, un recurso compartido de archivos o una cuenta de Azure Blob Storage. Para obtener una lista de almacenes de datos compatibles, consulte el artículo actividad de copia.*
>> - *Para representar un recurso de proceso que puede hospedar la ejecución de una actividad. Por ejemplo, la actividad HDInsightHive se ejecuta en un clúster de Hadoop para HDInsight. Consulte el artículo sobre transformación de datos para ver una lista de los entornos de proceso y las actividades de transformación admitidos.*


**Desencadenadores** *Los desencadenadores representan una unidad de procesamiento que determina cuándo es necesario poner en marcha una ejecución de canalización*


 **Flujos de datos**

 **Flujos de Control** *orquestación de actividades de canalización que incluye el encadenamiento de actividades en una secuencia, la bifurcación, la definición de parámetros en el nivel de canalización y el paso de argumentos mientras se invoca la canalización a petición o desde un desencadenador*

 **Vriables** *Las variables se pueden usar dentro de las canalizaciones para almacenar valores temporales y también se pueden usar junto con parámetros para habilitar el paso de valores entre canalizaciones, flujos de datos y otras actividades.*

 **Integration Runtime**
*Una instancia de Integration Runtime proporciona el puente entre la actividad y los servicios vinculados y define una actuación que se realizará. La actividad o servicio vinculado hace referencia a la instancia*

**Canalización** *una agrupación lógica de actividades para realizar una unidad de trabajo. Juntas, las actividades de una canalización realizan una tarea*[ejecutada secuencialmente o en paralelo]*.Por ejemplo, una canalización puede contener un grupo de actividades que ingiere datos de un blob de Azure y luego ejecutar una consulta de Hive en un clúster de HDInsight para particionar los datos.*

**Actividad** Es la unidad en el espacio de Canalizaciones. Es decir, las canalizaciones se constituyen de agrupaciones de actividades.            

    CanalizaciónNumeroA = ActividadNumeroAx(ActividadNumeroB + ActividadNumeroS)

Se admiten tres tipos de actividades (es decir tres tipos de unidad)

    - Actividad tipo Movimiento de Datos
    - Actividad tipo Transformación de Datos
    - Actividad tipo Control 

**Azure HDInsight** es un nproducto de azure (cuyos documentos están en [**este lugar**][r2]). Según ellos:


>*_ **Azure HDInsight** es un servicio de análisis, de código abierto, espectro completo y totalmente administrado en la nube para empresas. Con HDInsight, puede usar plataformas de código abierto, como Apache Spark, Apache Hive, LLAP, Apache Kafka, Hadoop, etc., en el entorno de Azure.*

**Azure Synapse Analytics**



**Azure Databricks** 

 
**Azure SQL Database**

**Azure Data Lake Storage**

**Azure Data Warehouse**

**Azure SQL Database**

**Azure Cosmos***

## Referencias 

[Docs for Data Factory][r0]

[Microsoft Intro Data Factory][r1]

[HDInsight][r2]: https://learn.microsoft.com/es-es/azure/hdinsight/

[Data Factory Visualización][r3]

[Actividad de Copia][r4]


[MiddleHolder][rINFINITOCERO]


[r0]:https://learn.microsoft.com/es-es/azure/data-factory/
[r1]: https://learn.microsoft.com/es-es/azure/data-factory/introduction
[r2]: https://learn.microsoft.com/es-es/azure/hdinsight/
[r3]: C:\Users\Carri\OneDrive\Documentos\Dani\azure\EsquemaDataFactory
[r4]: https://learn.microsoft.com/es-es/azure/data-factory/copy-activity-overview


[About](/about/) 
