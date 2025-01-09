# Herramientas de Desarrollo con IA

Este repositorio contiene dos proyectos principales:
1. Asistente de Código IA para Chat - Un asistente de programación interactivo usando el modelo Qwen
2. Generación y Detección de Imágenes - Un conjunto de herramientas para generar y analizar imágenes usando Stable Diffusion y YOLO

## 🚀 Descripción General del Proyecto

### Asistente de Código IA para Chat
Un asistente de código potenciado por IA que proporciona ayuda de programación interactiva a través de una interfaz de chat moderna, utilizando el modelo Qwen mediante la API de Hugging Face.

**Demo en Vivo:**
- Local: http://localhost:5173
- Producción: [https://chat-ia-fawn.vercel.app](https://chat-ia-fawn.vercel.app/)

### Generación y Detección de Imágenes
Un conjunto completo de herramientas que combina Stable Diffusion para la generación de imágenes y YOLO para la detección de objetos, implementado como un notebook de Jupyter.

## 📁 Estructura del Repositorio

```
Hugginface/
├── Modelo_Api/
│   └── chat-ia/
│       ├── public/
│       │   └── index.html
│       ├── src/
│       │   ├── components/
│       │   │   ├── ChatInterface.tsx
│       │   │   └── ui/
│       │   │       ├── Button.tsx
│       │   │       ├── Avatar.tsx
│       │   │       ├── ScrollArea.tsx
│       │   │       ├── Card.tsx
│       │   │       └── TextArea.tsx
│       │   ├── App.js
│       │   └── index.js
│       └── package.json
│
├── Modelos_Local/
│   └── Model_Local.ipynb
│
└── README.md
```

## 💡 Características

### Asistente de Código IA para Chat
- Interfaz de chat moderna y responsive
- Resaltado automático de código con detección de lenguaje
- Copiado de código con un clic y retroalimentación visual
- Soporte para múltiples lenguajes de programación
- Características mejoradas de UX:
  - Desplazamiento automático a nuevos mensajes
  - Indicadores de escritura
  - Avatares para usuario y asistente
  - Marcas de tiempo en los mensajes

### Generación y Detección de Imágenes
- Generación de imágenes usando Stable Diffusion v1.5
- Detección de objetos usando YOLOS-tiny
- Soporte para aceleración GPU
- Detección de objetos de alta confianza (umbral 0.9)
- Soporte para imágenes locales y desde URL
- Manejo integral de errores

## 🛠️ Tecnologías Utilizadas

### Asistente de Chat
- React
- API de Hugging Face Inference
- Tailwind CSS
- Shadcn/ui
- Lucide React
- TypeScript

### Procesamiento de Imágenes
- Hugging Face Hub
- Diffusers
- Transformers
- PyTorch
- Pillow
- Python 3.6+

## 📦 Instalación y Configuración

### Asistente de Chat
```bash
# Navegar al directorio del asistente de chat
cd chat-assistant

# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev
```

### Procesamiento de Imágenes
```bash
# Navegar al directorio de procesamiento de imágenes
cd image-processing

# Instalar paquetes de Python requeridos
pip install -r requirements.txt

# Iniciar Jupyter notebook
jupyter notebook
```

## ⚙️ Configuración

### Asistente de Chat
1. Obtener una clave de API de Hugging Face
2. Configurar variable de entorno: `HUGGING_FACE_API_KEY`
3. Opcional: Configurar ajustes del modelo

### Procesamiento de Imágenes
1. Crear una cuenta en Hugging Face
2. Iniciar sesión en Hugging Face Hub
3. Configurar ajustes de GPU si está disponible

## 💻 Uso

### Asistente de Chat
1. Ingresa tu pregunta de programación en la interfaz de chat
2. Recibe respuestas generadas por IA con explicaciones y ejemplos de código
3. Copia fragmentos de código con un clic
4. Navega por el historial de conversación dentro de la sesión

### Procesamiento de Imágenes
1. Cargar el notebook de Jupyter
2. Generar imágenes usando prompts de texto:
```python
prompt = "un astronauta montando a caballo en marte"
image = pipe(prompt).images[0]
image.save("astronauta_caballo.png")
```
3. Detectar objetos en imágenes:
```python
resultados = detectar_objetos("ruta/a/imagen.jpg")
# o
resultados = detectar_objetos("http://ejemplo.com/imagen.jpg")
```

## 🎯 Mejoras Futuras
- [ ] Soporte de imágenes/archivos en el chat
- [ ] Persistencia de mensajes
- [ ] Temas oscuros/claros
- [ ] Lenguajes de programación adicionales
- [ ] Exportación de conversaciones
- [ ] Búsqueda en el historial
- [ ] Opciones mejoradas de generación de imágenes
- [ ] Procesamiento por lotes para detección de objetos
- [ ] Soporte para entrenamiento de modelos personalizados

## 🤝 Contribución
1. Haz un fork del repositorio
2. Crea una rama para tu función (`git checkout -b feature/NuevaFuncion`)
3. Realiza tus cambios (`git commit -m 'Agregar alguna NuevaFuncion'`)
4. Sube la rama (`git push origin feature/NuevaFuncion`)
5. Abre un Pull Request

## 📝 Licencia
Este proyecto está bajo la Licencia MIT

## ⭐️ Créditos
- Modelo Qwen: [Qwen/Qwen2.5-Coder-32B-Instruct](https://huggingface.co/Qwen/Qwen2.5-Coder-32B-Instruct)
- Stable Diffusion v1.5: [sd-legacy/stable-diffusion-v1-5](https://huggingface.co/sd-legacy/stable-diffusion-v1-5)
- YOLOS-tiny: [hustvl/yolos-tiny](https://huggingface.co/hustvl/yolos-tiny)
- Componentes UI: [shadcn/ui](https://ui.shadcn.com/)
- Iconos: [Lucide](https://lucide.dev/)