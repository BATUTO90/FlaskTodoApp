# 🎨 HyperReal Studio 916

Generador de retratos hiperrealistas impulsado por agentes de IA y modelos de difusión de última generación de Hugging Face.

## 🚀 Características

- **Agentes de IA:** Utiliza un sistema de agentes para refinar prompts y mejorar la calidad de la imagen (iluminación, textura, composición, etc.).
- **Modelo de Alta Calidad:** Integrado con `stabilityai/stable-diffusion-xl-base-1.0` para resultados fotorrealistas superiores.
- **Optimizado para GPU:** Detecta y utiliza automáticamente una GPU (CUDA) para una generación de imágenes mucho más rápida.
- **Seguridad de API:** Gestiona el token de la API de Hugging Face de forma segura a través de variables de entorno.
- **Interfaz Intuitiva:** Interfaz de usuario sencilla y potente creada con Gradio.

## ⚙️ Requisitos Previos

- Python 3.8 o superior
- `pip` (el gestor de paquetes de Python)

## 💻 Instalación y Uso Local

1.  **Clona el repositorio:**
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd <NOMBRE_DEL_DIRECTORIO>
    ```

2.  **Instala las dependencias:**
    Crea un entorno virtual (recomendado) y activa la instalación de los paquetes.
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Configura tu Token de Hugging Face:**
    Necesitas un token de API de Hugging Face para descargar el modelo.
    -   Obtén tu token desde [Hugging Face Settings](https://huggingface.co/settings/tokens).
    -   Establece el token como una variable de entorno.

    En Linux/macOS:
    ```bash
    export HUGGING_FACE_TOKEN="tu_token_aqui"
    ```
    En Windows (Command Prompt):
    ```bash
    set HUGGING_FACE_TOKEN="tu_token_aqui"
    ```

4.  **Ejecuta la aplicación:**
    ```bash
    python app.py
    ```
    La aplicación se iniciará y podrás acceder a ella en tu navegador a través de la URL local que se mostrará en la terminal (normalmente `http://127.0.0.1:7860`).

## 🚀 Despliegue en Hugging Face Spaces

Hugging Face Spaces es una excelente opción para alojar y compartir esta aplicación de forma gratuita.

1.  **Crea un nuevo Space:**
    -   Ve a [Hugging Face Spaces](https://huggingface.co/new-space).
    -   Dale un nombre a tu Space.
    -   Selecciona **Gradio** como el SDK.
    -   Elige el hardware que prefieras (puedes empezar con una CPU básica, pero se recomienda una GPU para un mejor rendimiento).
    -   Haz clic en **Create Space**.

2.  **Sube tus archivos:**
    -   Sube los siguientes archivos a tu nuevo Space (puedes hacerlo a través de la interfaz web o usando `git`):
        -   `app.py`
        -   `requirements.txt`

3.  **Configura tu Token como un Secret:**
    Esta es la parte más importante para mantener tu token seguro.
    -   En tu Space, ve a la pestaña **Settings**.
    -   Busca la sección **Secrets** y haz clic en **New secret**.
    -   En el campo **Name**, escribe `HUGGING_FACE_TOKEN`.
    -   En el campo **Value**, pega tu token de Hugging Face.
    -   Haz clic en **Save secret**.

    La aplicación se reiniciará automáticamente y usará este *secret* como la variable de entorno `HUGGING_FACE_TOKEN`. ¡Tu aplicación ya está desplegada y lista para ser compartida!
