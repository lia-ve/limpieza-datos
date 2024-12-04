# Preprocesamiento y limpieza de datos

**Configurando tu Ambiente de Desarrollo Local**

Este proyecto utiliza el gestor de paquetes `uv` para las dependencias de Python. Para comenzar, necesitarás instalar `uv` y luego crear y activar un entorno virtual para tu proyecto.

### Instalando `uv`

1. **Requisitos previos:** Asegúrate de tener Python 3.12 o posterior instalado en tu sistema. Puedes verificar tu versión de Python ejecutando `python --version` o `python3 --version` en tu terminal.

2. **Instalar `uv`:** Abre tu terminal y ejecuta el siguiente comando:

   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

También puedes utilizar el sistema de paquetes de tu distribución de linux o usar `pipx`.

### Creando y Activando el Entorno Virtual

1. **Navega al directorio de tu proyecto.** Utiliza el comando `cd` en tu terminal para navegar al directorio donde tienes los archivos de tu proyecto, incluyendo el archivo `pyproject.toml`.

2. **Crea el entorno virtual:** Ejecuta el siguiente comando en tu terminal:

   ```bash
   uv venv
   ```

   Esto creará un nuevo entorno virtual llamado `.venv` en tu directorio de proyecto. El entorno virtual aísla las dependencias de tu proyecto de la instalación de Python de tu sistema.

3. **Activa el entorno virtual:** El proceso de activación depende de tu sistema operativo:

   * **Windows:** Ejecuta el siguiente comando:

     ```bash
     .venv\Scripts\activate.bat
     ```

   * **macOS/Linux:** Ejecuta el siguiente comando:

     ```bash
     source .venv/bin/activate
     ```

   Tu terminal mostrará el nombre del entorno virtual activo (por ejemplo, `(limpieza-datos) `) para indicar que está activado.

   Si estás trabajando en vscode selecciona el python dentro del entorno como el intérprete del proyecto.

### Instalando Dependencias

Una vez que hayas activado el entorno virtual, puedes instalar las dependencias del proyecto usando `uv`:

```bash
uv pip install -r pyproject.toml
```

Este comando leerá el archivo `pyproject.toml` e instalará todos los paquetes requeridos (`jupyterlab`, `matplotlib`, `pandas`, etc.) en tu entorno virtual.

**Notas adicionales:**

* Para desactivar el entorno virtual, simplemente ejecuta el siguiente comando en tu terminal:

  ```bash
  deactivate
  ```

* Recuerda activar el entorno virtual cada vez que quieras trabajar en el proyecto para asegurarte de que estás utilizando el conjunto correcto de dependencias.
