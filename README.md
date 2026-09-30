# Catálogo de Recursos Académicos

## Descripción
Este proyecto tiene como objetivo organizar y consultar recursos académicos de manera sencilla y estructurada. Permite mantener una base de datos de materiales útiles para estudio, investigación y referencia, facilitando su clasificación y búsqueda.

## Objetivo
Crear una solución inicial para registrar recursos educativos y académicos, con una organización clara por tipo, tema, nivel y fuente, para apoyar la consulta y administración de información relevante.

## Estructura general
- `app/`: lógica principal de la aplicación.
- `data/`: archivos de datos, por ejemplo recursos en formato JSON.
- `docs/`: documentación del proyecto.
- `tests/`: pruebas iniciales y validaciones básicas.
- `requirements.txt`: dependencias del entorno.

## Tecnologías utilizadas
- Python 3
- JSON para almacenamiento de datos
- Markdown para documentación
- pytest para pruebas básicas

## Preparación del entorno
1. Crear un entorno virtual:
   ```bash
   python -m venv .venv
   ```
2. Activar el entorno virtual:
   - Windows:
     ```bash
     .\.venv\Scripts\activate
     ```
   - macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```
3. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```

## Dependencias
El proyecto utiliza las bibliotecas y herramientas necesarias para ejecutar pruebas y mantener una base de datos básica. Si se agregan nuevas dependencias en el futuro, deben registrarse en `requirements.txt`.

## Uso inicial
Ejecuta la aplicación desde la carpeta principal:
```bash
python app/main.py
```

## Próximas mejoras
- Añadir una interfaz más amigable para consultar recursos académicos.
- Incorporar filtros por tipo, tema, nivel y autor.
- Permitir guardar recursos favoritos y exportarlos en distintos formatos.
- Mejorar la validación y la gestión de datos en el archivo JSON.
- Expandir la documentación con ejemplos de uso y casos de prueba.
