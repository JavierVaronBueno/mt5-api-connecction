# Conexión a MetaTrader 5 con Python

Este repositorio contiene un Jupyter Notebook diseñado para interactuar con la plataforma MetaTrader 5 utilizando Python. Este proyecto es ideal para traders y desarrolladores interesados en automatizar operaciones, analizar datos de mercado y desarrollar estrategias de trading. Está específicamente configurado para trabajar con la terminal **Darwinex**, pero puede adaptarse a otros brokers compatibles con MetaTrader 5.

## Características principales

- **Conexión a MetaTrader 5**: Configura y conecta automáticamente la terminal de trading a través de Python.
- **Ejecución de órdenes de mercado**: Proporciona las bases para ejecutar operaciones directamente desde tu código.
- **Recuperación de datos históricos**: Obtén datos históricos para análisis y desarrollo de estrategias.
- **Gestión de credenciales y configuración**: Sistema seguro y ordenado para almacenar configuraciones y credenciales del usuario.

---

## Requisitos previos

Antes de usar este proyecto, asegúrate de cumplir con los siguientes requisitos:

1. **Python 3.11**: Este proyecto requiere Python 3.11 para garantizar la compatibilidad con la librería MetaTrader5.
2. **MetaTrader 5**: Descarga e instala MetaTrader 5, preferiblemente la terminal de Darwinex para un ejemplo directo.
3. **Anaconda**: Necesario para la gestión de entornos virtuales y dependencias.
4. **Visual Studio Code (opcional)**: Recomendado para editar y ejecutar el Jupyter Notebook.

---

## Configuración del entorno virtual

Sigue estos pasos para configurar un entorno virtual en Anaconda y preparar el proyecto:

1. **Crear el entorno virtual:**
   ```bash
   conda create --name mt5API python=3.11
   ```
   Esto creará un entorno virtual llamado `mt5API` con Python 3.11.

2. **Activar el entorno virtual:**
   ```bash
   conda activate mt5API
   ```

3. **Instalar dependencias necesarias:**
   - **Pandas**:
     ```bash
     pip install pandas
     ```
   - **MetaTrader 5**:
     ```bash
     pip install MetaTrader5
     ```
   - **IPython Kernel** (para Jupyter Notebooks):
     ```bash
     pip install ipykernel
     ```

4. **Registrar el kernel en Jupyter:**
   ```bash
   python -m ipykernel install --user --name=mt5API
   ```

---

## Instrucciones de uso

1. **Clona este repositorio:**
   ```bash
   git clone https://github.com/JavierVaronBueno/mt5-api-connecction.git
   cd mt5-api-connecction
   ```

2. **Abre el Jupyter Notebook en Visual Studio Code o JupyterLab.**
   - Asegúrate de seleccionar el kernel del entorno virtual creado (`mt5API`) antes de ejecutar las celdas.

3. **Configura tus credenciales:**
   - Edita el diccionario de credenciales dentro del Notebook con los detalles de tu cuenta:
     - Ruta de instalación de MetaTrader 5.
     - Login.
     - Contraseña.
     - Servidor del broker.

4. **Ejecuta las celdas del Notebook:**
   - Verifica la conexión con MetaTrader 5.
   - Realiza pruebas iniciales, como obtener datos de mercado o iniciar operaciones.

---

## Estructura del proyecto

```
mt5API/
│
├── mt5_connect.ipynb   # Jupyter Notebook principal
├── README.md           # Documentación del proyecto
└── .gitignore          # Archivos a ignorar en Git
```

- **`mt5_connect.ipynb`**: Contiene todo el código necesario para interactuar con MetaTrader 5.
- **`README.md`**: Este archivo con instrucciones detalladas.
- **`.gitignore`**: Evita subir archivos sensibles o temporales al repositorio.

---

## Notas importantes

1. **Uso de credenciales de demo**:
   - Para evitar problemas y riesgos, utiliza una cuenta demo durante las pruebas iniciales.
2. **Adaptación a otros brokers**:
   - Cambia el nombre del servidor en las credenciales si estás utilizando otro broker que no sea Darwinex.
3. **Compatibilidad con MetaTrader 5**:
   - Asegúrate de que la ruta del terminal de MetaTrader 5 es correcta, incluyendo el archivo `terminal64.exe`.

---

## Errores comunes y soluciones

| **Error**                                   | **Causa**                              | **Solución**                                                                 |
|---------------------------------------------|----------------------------------------|------------------------------------------------------------------------------|
| `ModuleNotFoundError: No module named 'MetaTrader5'` | Librería no instalada en el entorno   | Instala la librería usando `pip install MetaTrader5`.                        |
| Conexión fallida con MetaTrader 5           | Credenciales incorrectas o servidor mal configurado | Revisa y corrige las credenciales en el diccionario de configuración.        |
| Kernel incorrecto seleccionado en Jupyter   | Kernel de Python no vinculado al entorno virtual | Selecciona el kernel `mt5API` en la interfaz de Jupyter.                 |

---

## Cómo contribuir

¡Contribuir a este proyecto es fácil! Sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama para tus cambios:
   ```bash
   git checkout -b nueva-funcionalidad
   ```
3. Haz tus cambios y realiza un commit:
   ```bash
   git commit -m "Agrega nueva funcionalidad"
   ```
4. Sube tus cambios al repositorio:
   ```bash
   git push origin nueva-funcionalidad
   ```
5. Abre un Pull Request describiendo tus cambios.

---

## Licencia

Este proyecto está licenciado bajo la [Licencia MIT](https://opensource.org/licenses/MIT). Puedes usar, modificar y distribuir este código bajo los términos de esta licencia.
