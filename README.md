Extracción y almacenamiento de Datos desde la API de Rick and Morty

Este proyecto implementa un script en Python para automatizar el ciclo completo de extracción de datos
desde una API pública (The Rick and Morty API). 
El foco está en aplicar buenas prácticas de desarrollo: evitar el hardcoding mediante variables de entorno, 
manejar errores de conexión de forma robusta, transformar la estructura con Pandas y asegurar la persistencia en un archivo CSV.

El proyecto utiliza las siguientes librerías de Python:

    requests: Para realizar las peticiones HTTP a la API.

    python-dotenv: Para cargar de forma segura la URL desde un archivo de configuración.

    pandas: Para la limpieza, filtrado y estructuración de los datos en formato tabular.

Para instalarlas, ejecuta:
Bash

pip install requests python-dotenv pandas

Estructura del Repositorio
Plaintext

├── 📄 pre_entrega_4.ipynb    # el código paso a paso
├── 📄 data_extracted.csv     # Archivo con los datos limpios
├── 📄 .env                   # Archivo de configuración con la URL de la API
├── 📄 .gitignore             # Archivo para excluir cachés y entornos virtuales
└── 📄 README.md              # Documentación del proyecto

detarlle del desarrollo
·Seguridad y Configuración (.env):
·Se utiliza un archivo .env para almacenar la URL (API_URL=[https://rickandmortyapi.com/api/character](https://rickandmortyapi.com/api/character)), 
evitando escribir valores fijos directamente en el código fuente.
·Extracción con Manejo de Errores (try-except):
El script se conecta a la API validando el tiempo de respuesta (timeout) y los códigos de estado HTTP. 
Si ocurre un fallo de red o un error del servidor, el programa lo intercepta y muestra un mensaje claro 
sin interrumpir bruscamente.
·Transformación Básica (Pandas):
La respuesta en formato JSON se convierte en una base de datos. Luego se filtran las columnas innecesarias 
para conservar únicamente los campos clave: id, name, status, species y gender.
·Persistencia de Datos:
El conjunto de datos limpio se exporta y guarda automáticamente en la raíz del entorno como un archivo estructurado bajo el nombre de data_extracted.csv.

Cómo Ejecutar el Proyecto
descargar en computadora todos los archivos subidos al repositorio para su funcionamiento correcto

    Asegúrate de tener el archivo .env configurado con la ruta de la API.

    Ejecuta el código secuencialmente para generar el archivo CSV y dejarlo listo para su entrega.
