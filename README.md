# 🌟 Galenus AI: Asistente Médico Inteligente 🌟

**Versión:** 2.0  
**Autor:** Alexander Saravia  
**Fecha:** 12/01/2025  

## 📖 Descripción del Proyecto

**Galenus AI** es un asistente inteligente diseñado para brindar recomendaciones e insights sobre síntomas y recetas médicas. Este sistema analiza documentos médicos como imágenes, audio, PDF, Excel, y Word, proporcionando contextos relevantes, realizando búsquedas en la web y gestionando conocimiento a través de una arquitectura modular y escalable.

Este proyecto combina lo mejor de las tecnologías modernas para ofrecer una solución eficiente, segura y orientada a las necesidades médicas.

---

## 🛠️ Tecnologías Utilizadas

| Tecnología        | Uso                                                                                   |
|--------------------|---------------------------------------------------------------------------------------|
| **Python** 🐍     | Desarrollo del backend y microservicios (FastAPI).                                    |
| **Docker** 🐳     | Contenerización de los servicios para despliegue y escalabilidad.                     |
| **PostgreSQL** 🐘 | Persistencia de datos: almacenamiento de logs y gestión de roles.                     |
| **Redis** 🏎️      | Caché de datos para mejorar el rendimiento (manejo de tokens y consultas frecuentes). |
| **OpenSearch** 🔍 | Base de conocimiento vectorial (alternativa: ChromaDB).                              |
| **Flask** 🍰      | Orquestación de servicios y punto de acceso a la interfaz web.                        |

---

## 🚀 Características Principales

### 🎯 Asistente IA
- Responde preguntas médicas basadas en síntomas y recetas.
- Genera recomendaciones contextuales apoyadas por búsquedas en la web.

### 🗂️ Procesamiento de Documentos
- Soporte para múltiples formatos: imágenes, audio, PDF, Excel, Word, etc.
- Análisis detallado y extracción de insights.

### ⚙️ Arquitectura Modular
- **Orquestador de Entradas**: Administra y distribuye los datos a los procesadores correspondientes.
- **Procesadores especializados**:
  - **Texto** 📝
  - **Imágenes** 🖼️
  - **Audio** 🎙️
- **Organizador de Conocimiento**: Integra los datos procesados en una base vectorial.

### 🧠 Base de Conocimiento
- **OpenSearch** o **ChromaDB**: Almacenamiento y recuperación de información relevante utilizando embeddings vectoriales.

### 🔒 Seguridad
- Integración con roles y permisos para garantizar accesos controlados.
- Implementación de protocolos HTTPS para la protección de datos.

---

## 📊 Estructura de la Arquitectura

![Arquitectura Conceptual](galenus.drawio.png)

### Componentes Clave
1. **Asistente IA**: Motor principal que integra procesadores y la base de conocimiento.
2. **Orquestador de Entradas**: Gestiona y enruta documentos a los procesadores adecuados.
3. **Procesadores**: Analizan datos en diferentes formatos.
4. **Cache 1 y Cache 2**: Redis para optimización de consultas.
5. **Base de Conocimiento**: Recupera información clave de forma eficiente.
6. **Logs** y **Roles**: Manejo de datos de interacción y control de acceso.

---

## 🌐 Cómo Ejecutar el Proyecto

### 1️⃣ Prerrequisitos
- Docker 🐳
- Python 3.9+ 🐍
- Redis 🏎️
- PostgreSQL 🐘
- OpenSearch o ChromaDB 🔍

### 2️⃣ Configuración
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tuusuario/galenus-ai.git
   cd galenus-ai
   ```
2. Configura las variables de entorno en un archivo `.env`:
   ```
   POSTGRES_USER=usuario
   POSTGRES_PASSWORD=contraseña
   REDIS_URL=redis://localhost:6379
   OPENSEARCH_URL=http://localhost:9200
   ```

### 3️⃣ Despliegue
- Usa **Docker Compose** para ejecutar los servicios:
  ```bash
  docker-compose up -d
  ```

---

## 🛡️ Seguridad y Buenas Prácticas

- **Cifrado de datos**: Implementa HTTPS para las comunicaciones entre cliente y servidor.
- **Gestión de secretos**: Utiliza herramientas como HashiCorp Vault para almacenar claves sensibles.
- **Monitoreo**: Incorpora Prometheus y Grafana para métricas y visualización.

---

## 🛠️ Futuras Mejoras

- Implementación de Graph RAG para un análisis más detallado.
- Escalabilidad a Kubernetes para manejo de mayor tráfico.
- Soporte para nuevos formatos de documentos y modelos de análisis avanzados.

---

## 🤝 Contribuciones

¡Eres bienvenido a contribuir! Abre un issue o crea un pull request con tus sugerencias y mejoras. 🚀

---

Espero que esta descripción sea útil para tu repositorio en GitHub. ¡Avísame si necesitas más detalles! 🎉
