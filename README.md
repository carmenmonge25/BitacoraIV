# 

# 

# 

# UD07. Elaboración de documentación técnica y uso de aplicaciones de propósito general

**Tabla de contenido:**

[**I. Sprint 1: El Marco Legal y la Estructura del "Relato"	1**](#i.-sprint-1:-el-marco-legal-y-la-estructura-del-"relato")

[1.1. Tarea 1: El Escudo Legal	1](#1.1.-tarea-1:-el-escudo-legal)

[1.2. Tarea 2: La Memoria Técnica (Estructura Ofimática)	1](#1.2.-tarea-2:-la-memoria-técnica-\(estructura-ofimática\))

[1.3. Tarea 3: Análisis de Necesidades (Tu primer texto técnico)	2](#1.3.-tarea-3:-análisis-de-necesidades-\(tu-primer-texto-técnico\))

[**II. Sprint 2: Infraestructura Cloud, Transferencia de Ficheros y El Investigador	2**](#ii.-sprint-2:-infraestructura-cloud,-transferencia-de-ficheros-y-el-investigador)

[2.1. Tarea 1: La Hoja de Costes	2](#2.1.-tarea-1:-la-hoja-de-costes)

[**2.2. Tarea 2: Red y Comunicación	3**](#2.2.-tarea-2:-red-y-comunicación)

[**2.3. Tarea 3: El Investigador	3**](#2.3.-tarea-3:-el-investigador)

# I. Sprint 1: El Marco Legal y la Estructura del "Relato" {#i.-sprint-1:-el-marco-legal-y-la-estructura-del-"relato"}

## 1.1. Tarea 1: El Escudo Legal {#1.1.-tarea-1:-el-escudo-legal}

(El archivo LICENSES.md)

No podemos usar software en una empresa sin saber si es legal hacerlo. Y no, "es gratis" no es una categoría legal.

**Instrucciones paso a paso**:

1. Entra en la carpeta raíz de tu repositorio de la Bitácora 4\.  
2. Crea un nuevo archivo llamado LICENSES.md.  
3. Investiga y redacta en ese archivo qué licencia tiene cada pieza de tu infraestructura. Para cada una, debes indicar el nombre del software, su licencia y un enlace a la fuente oficial.  
   1. **Ejemplo**: *PostgreSQL se distribuye bajo la Licencia PostgreSQL (una licencia permisiva de tipo open source similar a la BSD o MIT)*.  
4. Debes incluir **obligatoriamente**: Apache Guacamole y OpenSSH.

**¿Por qué hacemos esto?** Porque según el CE a), debes ser capaz de clasificar el software según su propósito y su licencia.

## 1.2. Tarea 2: La Memoria Técnica (Estructura Ofimática) {#1.2.-tarea-2:-la-memoria-técnica-(estructura-ofimática)}

Vamos a crear el documento donde contaréis vuestra "hazaña" técnica. No vale un documento plano; queremos nivel profesional.

**Instrucciones paso a paso**:

1. En tu repositorio, crea una carpeta llamada docs.  
2. Abre tu procesador de textos (Google Docs) y crea un archivo llamado Memoria\_Tecnica\_SI\_Apellido.md  
3. **Configura el esqueleto**:  
   * **Portada**. Título del proyecto, tu nombre, ciclo y fecha.  
   * **Índice Automático**. No lo escribas a mano. Usa la herramienta de "Tabla de contenidos".  
   * **Jerarquía de títulos**. Configura el "Título 1" para las secciones principales y el "Título 2" para los apartados; el “Título 3”, sólo si lo consideras necesario.  
4. Guarda el archivo dentro de la carpeta docs de tu repositorio (mientras lo terminas puedes utilizar Google Drive).

## 1.3. Tarea 3: Análisis de Necesidades (Tu primer texto técnico) {#1.3.-tarea-3:-análisis-de-necesidades-(tu-primer-texto-técnico)}

Es hora de justificar tu trabajo. No instalaste Docker porque sí.

**Instrucciones paso a paso**:

1. Ve al apartado "**1\. Análisis de Necesidades**" de tu memoria.  
2. Redacta una explicación (mínimo 350 palabras) respondiendo a esto:  
   * ¿Qué problema de la empresa resolvemos con Guacamole y Docker? (*Pista: centralización, ahorro de recursos, seguridad…*).  
   * ¿Por qué elegimos esta solución y no conectar directamente por RDP a cada máquina?  
3. Usa un lenguaje técnico pero claro. Recuerda que eres un profesional, que nadie más que tu sabe de lo que habla, y recuerda, que esto lo leerá tu jefe.

**Referencia académica para tu texto**. Según la ingeniería de software, un buen análisis de requisitos evita fallos críticos en la producción.

# II. Sprint 2: Infraestructura Cloud, Transferencia de Ficheros y El Investigador {#ii.-sprint-2:-infraestructura-cloud,-transferencia-de-ficheros-y-el-investigador}

## 2.1. Tarea 1: La Hoja de Costes {#2.1.-tarea-1:-la-hoja-de-costes}

Un buen código que arruina al cliente en servidores es un fracaso. Vamos a calcular el Coste Total de Propiedad (TCO) mensual de vuestra infraestructura.

**Instrucciones paso a paso:**

1. Abre una herramienta de Hoja de Cálculo (Google Sheets).  
2. Crea un libro llamado Presupuesto\_Cloud\_Proyecto.  
3. Diseña una tabla profesional (usa logo y colores corporativos, bordes, celdas combinadas para los títulos) que calcule el coste mensual de alojar vuestra aplicación. Debe incluir:  
   * **Cómputo (Servidor VPS / Contenedores):** Ej. AWS EC2, Google Cloud, DigitalOcean Droplet, etc.  
   * **Almacenamiento (Base de Datos / Discos):** Coste por GB.  
   * **Transferencia de Red (Ancho de banda):** Coste por tráfico saliente.  
4. Utiliza fórmulas (SUMA, multiplicaciones) para calcular el subtotal y añade una celda que calcule el IVA (21%) para obtener el Total Mensual.  
5. **Integración:** Exporta la tabla como PDF o toma una captura de alta calidad y añádela al archivo Memoria\_Tecnica\_SI\_Apellido.md en un nuevo apartado llamado **"2. Estimación de Costes de Infraestructura"**.

## 2.2. Tarea 2: Red y Comunicación {#2.2.-tarea-2:-red-y-comunicación}

¿Cómo llega tu código del PC de tu casa al servidor real?

**Instrucciones paso a paso:**

1. En tu memoria técnica, crea el apartado **"3. Estrategia de Despliegue y Comunicación"**.  
2. Redacta (aprox. 150 palabras) qué sistema de transferencia de ficheros vas a utilizar para mover tu aplicación a producción y justifica por qué es seguro. *(Debes mencionar explícitamente si usarás SFTP, FTPS o integraciones Cloud nativas, descartando el FTP tradicional en texto plano).*  
3. **Mensajería:** Añade un pequeño párrafo explicando cómo tu equipo va a utilizar herramientas de mensajería (Slack, Google Chat, Microsoft Teams o Discord) para comunicarse incidencias técnicas o recibir alertas automáticas si el servidor se cae.

## 2.3. Tarea 3: El Investigador {#2.3.-tarea-3:-el-investigador}

Toca darle rigor universitario a tu documentación. Vamos a justificar una tecnología de tu proyecto (por ejemplo: la seguridad en Docker, el rendimiento de PostgreSQL frente a MongoDB, o el impacto de la arquitectura Cloud).

**Instrucciones paso a paso:**

1. Accede a **Google Académico**, **DOAJ** o **Dialnet**.  
2. Busca un artículo científico o Tesis publicado en los últimos 5 años sobre la tecnología que estás usando.  
3. En tu memoria, crea el apartado **"4. Justificación Científica"**.  
4. Redacta un párrafo donde resumas la conclusión de ese artículo y cómo apoya tu proyecto.  
5. **Cita obligatoria:** Añade al final de tu memoria un apartado de **"Referencias"** y cita el artículo utilizando estrictamente el formato **IEEE**.  
   * *Ejemplo IEEE:* J. Pérez y A. Gómez, "Análisis de rendimiento en bases de datos NoSQL para entornos Cloud," *Revista de Ingeniería Web*, vol. 4, no. 2, pp. 45-56, 2024\.

