🚀 Nexus Jarvis Automation Suite
Python React Vercel SAP RPA AI Vision

Plataforma Web Centralizada para la Orquestación y Monitoreo de Bots de Automatización Logística (RPA + IA).

💡 Visión General
Nexus Orchestrator es una solución Full-Stack diseñada para transformar la gestión de procesos logísticos. Pasa de scripts de automatización individuales y descentralizados a una Plataforma de Gestión de Bots (BMS) accesible vía web. Permite a los usuarios operativos lanzar, monitorear y gestionar flujos de trabajo automatizados en SAP ERP y otras aplicaciones, optimizando la eficiencia y la visibilidad.

VER DEMO EN VIVO: [Deploy with Vercel]

🎯 Problema de Negocio Resuelto
En entornos logísticos dinámicos, la dependencia de procesos manuales en SAP y la dificultad de gestionar múltiples scripts de automatización generan:

Ineficiencias operativas.
Errores humanos recurrentes.
Falta de visibilidad sobre el estado de la automatización.
Cuellos de botella administrativos y operacionales.
Nexus Orchestrator aborda estos desafíos proporcionando un punto de control unificado.

✅ Solución Tecnológica
La plataforma se compone de dos capas principales:

Frontend Web (Interfaz de Usuario): Una aplicación moderna y responsiva construida con React/Next.js, desplegada en Vercel. Permite a los usuarios seleccionar los bots, ingresar parámetros y visualizar el estado de las ejecuciones.

Screenshot de la Interfaz Web (Asegúrate de que esta imagen no contenga información sensible, como tu ruta de OneDrive o datos internos. Recórtala o edítala si es necesario.)

Backend & Orquestador (Python): Un servicio en Python que actúa como el cerebro de la suite. Recibe las solicitudes del frontend, gestiona la ejecución de los bots individuales (workers), maneja la lógica de negocio y mantiene un registro de eventos.

Bots Workers (RPA & IA): Una flota de bots individuales (desarrollados en Python con CustomTkinter para interacción local si aplica, o como scripts de consola puros) que realizan las tareas específicas en SAP GUI o interactúan con APIs externas.

⚙️ Módulos de la Suite
Nexus Orchestrator gestiona los siguientes "productos" de automatización:

Ingesta Masiva (MIGO):

Función: Automatiza la carga de movimientos de mercancías en SAP (MIGO) desde un archivo Excel, optimizando procesos de traspaso y recepción.
Impacto: Reduce drásticamente los tiempos de digitación y minimiza errores.
Optimizador de Altura (LX02):

Función: Genera reportes visuales de ubicaciones de stock en altura desde LX02, facilitando la auditoría física y la gestión del espacio.
Impacto: Mejora la eficiencia de la auditoría de almacenes complejos.
Guardián de Stock ("Zombies"):

Función: Audita stocks y tránsitos "zombies" (inmovilizados) en SAP MM (cruces MB52 vs MB51).
Impacto: Proporciona alertas tempranas para la recuperación de capital y previene mermas por obsolescencia.
Visión Operacional (IA):

Tecnología: Utiliza la API de Google Gemini (Visión Artificial).
Función: Digitaliza y procesa información manuscrita de pizarras de andén para integrarla con Power BI, ofreciendo visibilidad sobre operaciones no digitalizadas.
Monitor Logístico:

Función: Extrae y consolida datos de transacciones de transporte (VT11, VT03N) para generar reportes o notificaciones automáticas sobre el estado de la flota y despachos.
Orquestador de Traspasos: (Breve descripción si es un bot real, ej: Gestiona y automatiza la secuencia de traspasos entre ubicaciones.)

Sincronizador de Maestros: (Breve descripción si es un bot real, ej: Automatiza la actualización y consistencia de datos maestros de materiales o proveedores.)

💻 Arquitectura Técnica
El proyecto sigue una arquitectura orientada a servicios para modularidad y escalabilidad.

Nexus-Orchestrator-Logistics/
├── web-app/                  # Frontend de la aplicación web (React/Next.js)
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── ...
├── backend-orchestrator/     # Backend y lógica de orquestación (Python)
│   ├── main.py               # API REST (FastAPI/Flask)
│   ├── requirements.txt
│   ├── bots/                 # Scripts de automatización (workers)
│   │   ├── __init__.py
│   │   ├── sap_bot_auditor.py
│   │   ├── sap_bot_migo.py
│   │   └── ...
│   └── ...
├── deploy/                   # Scripts de despliegue (Docker/Vercel config)
├── assets/                   # Recursos visuales (screenshots, iconos)
├── .github/                  # Configuración de GitHub (CI/CD si aplica)
└── README.md
