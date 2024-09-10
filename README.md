# Análisis de Calidad del Aire en Ciudades de India

Este proyecto realiza un análisis detallado de la calidad del aire en varias ciudades de India, diferenciando entre zonas industriales y residenciales. El objetivo es identificar patrones de contaminación y sus principales contribuyentes, basándose en datos históricos de AQI (Índice de Calidad del Aire) y diferentes contaminantes.

## Requisitos

Para ejecutar el notebook correctamente, necesitarás las siguientes herramientas y bibliotecas de Python:

### Herramientas

- **Python 3.7+**
- **Jupyter Notebook** o cualquier entorno que soporte notebooks de Jupyter, como **JupyterLab** o **VSCode**.
- **Kaggle API**: Para descargar el dataset desde Kaggle.

### Instalación de dependencias

1. Clona el repositorio en tu máquina local:

   ```bash
   git clone https://github.com/tu-repo/calidad-aire-india.git
   cd calidad-aire-india
   ```

2. Crea y activa un entorno virtual (opcional pero recomendado):

   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scriptsctivate
   ```

3. Instala las dependencias requeridas utilizando el archivo `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

### Bibliotecas requeridas

El proyecto requiere las siguientes bibliotecas de Python:

- `pandas`: Para manipulación y análisis de datos.
- `numpy`: Para cálculos numéricos y manejo de arrays.
- `matplotlib`: Para visualización de datos.
- `seaborn`: Para la creación de gráficos estadísticos.
- `scikit-learn`: Para el preprocesamiento de datos y modelos de machine learning.
- `kaggle`: Para descargar el dataset desde Kaggle.

### Estructura del proyecto

- `notebook.ipynb`: El notebook principal que contiene el análisis de datos y visualizaciones.
- `data/`: Carpeta donde se almacenan los archivos de datos necesarios para ejecutar el análisis.
- `kaggle.json`: Archivo con las credenciales de la API de Kaggle para descargar la base de datos.
- `requirements.txt`: Archivo de dependencias para instalar todas las bibliotecas necesarias.
- `README.md`: Guía de uso y ejecución del proyecto.

### Descarga e instalación del dataset desde Kaggle

Primero, asegúrate de tener instaladas las siguientes bibliotecas en tu notebook o entorno Python:

```python
!pip install kaggle
```

Luego, descarga el dataset desde Kaggle usando la API:

```python
!kaggle datasets download -d rohanrao/air-quality-data-in-india
```

Una vez descargado, descomprime el archivo ZIP para acceder a los datos. Puedes hacerlo directamente en el notebook utilizando el siguiente código:

```python
import zipfile

# Reemplaza 'air-quality-data-in-india.zip' con el nombre exacto del archivo si ha cambiado
with zipfile.ZipFile('air-quality-data-in-india.zip', 'r') as zip_ref:
    zip_ref.extractall()
```

Este código instala la API de Kaggle, descarga el dataset de calidad del aire en India y lo descomprime automáticamente en tu entorno de trabajo. Asegúrate de que el archivo `kaggle.json` esté correctamente ubicado en `~/.kaggle/` (Linux/Mac) o `C:\Users\<TuNombre>\.kaggle\` (Windows) antes de ejecutar la descarga.

### Ejecución del notebook

Abre el notebook en tu entorno preferido:

```bash
jupyter notebook notebook.ipynb
```

Ejecuta las celdas en el orden indicado para realizar el análisis. El notebook cargará los datos, realizará el preprocesamiento, generará las visualizaciones y mostrará los resultados del análisis.

### Notas importantes

- **Manejo de datos nulos**: Asegúrate de que los datos estén correctamente limpios, manejando los valores nulos y aplicando las transformaciones descritas en el notebook.

- **Normalización**: Las variables numéricas han sido normalizadas logarítmicamente y las variables categóricas se codificaron usando One-Hot Encoding.

### Contribuciones

Si deseas contribuir al proyecto, puedes abrir un Pull Request o reportar un Issue en el repositorio.

### Contacto

Si tienes alguna pregunta o sugerencia sobre el proyecto, no dudes en contactarme.
