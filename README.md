PEF Analytics System

¿La política monetaria de EE.UU. pesa más que la economía local en mercados emergentes?

Proyecto personal de data engineering con Azure, arquitectura Medallion y pipelines end-to-end.

---

Objetivo

Responder con datos una pregunta que me fascina: ¿quién tiene el poder real en mercados emergentes como Argentina? ¿La política monetaria de EE.UU. (Fed) o las condiciones económicas locales?

Este proyecto es mi campo de entrenamiento para aprender data engineering de verdad: escribiendo cada línea, resolviendo cada error, tomando cada decisión.

---

Pregunta de investigación

¿La política monetaria de EE.UU. (Fed) pesa más que la economía local en mercados emergentes como Argentina?

---

Stack tecnológico

· SO: Debian 12 en WSL2
· Cloud: Microsoft Azure
· Gestión: Azure CLI
· Orquestación: Azure Functions (Python)
· Almacenamiento: Azure Data Lake Storage Gen2
· Procesamiento: Python + PySpark
· Base de datos: Azure SQL Database (por definir)
· Control de versiones: Git + GitHub

---

Arquitectura (Medallion)

Fuentes de datos (World Bank API / FRED / INDEC)

Bronce (Raw Data)
Datos crudos tal cual se extraen de las APIs
Formato: JSON / Parquet

Silver (Cleaned Data)
Datos validados, limpieza de nulos, estandarización
Formato: Parquet

Gold (Aggregated Data)
Datos agregados listos para análisis y consultas SQL
Formato: Parquet / Azure SQL

---

Estructura del proyecto

PEF-Analytics-System/
├── src/
│   ├── ingest/
│   ├── transform/
│   ├── aggregate/
│   └── utils/
├── data/
│   ├── bronze/
│   ├── silver/
│   └── gold/
├── notebooks/
├── tests/
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md
  
---

Estado actual del proyecto

Configuración de entorno (Debian + WSL2 + Azure CLI): Completado
Resource Group y Storage Account: Completado
Function App configurada: Completado
Script de ingesta desde API: En desarrollo
Transformación a capa plata: Pendiente
Agregación a capa oro: Pendiente
Análisis y conclusiones: Pendiente

---

Próximos pasos

1. Escribir script de ingesta con Python (requests + Azure SDK)
2. Subir datos al contenedor bronce
3. Deploy de Azure Function con timer trigger
4. Transformaciones con PySpark a capa plata
5. Consultas SQL en capa oro

---

Cómo ejecutar el proyecto (en desarrollo)

git clone https://github.com/dalmirorivaderacreator/PEF-Analytics-System.git
cd PEF-Analytics-System

python -m venv venv
source venv/bin/activate   # En Windows: venv\Scripts\activate

pip install -r requirements.txt

cp .env.example .env

Editar .env con tus credenciales de Azure

python src/ingest/world_bank_ingest.py

---

Aprendizajes hasta ahora

Este proyecto es mi verdadera escuela. Cada línea de código, cada error, cada solución queda registrada acá. No es un proyecto de curso ni generado por IA. Es 100 por ciento mío.

---

Licencia

MIT License. Ver el archivo LICENSE para más detalles.

---

Autor

Dalmiro Rivadera
Data Engineer en formación | Azure | Python | Linux

GitHub: https://github.com/dalmirorivaderacreator
LinkedIn: https://linkedin.com/in/dalmirorivadera

