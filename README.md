🚀 AI-CodeGuard: Microservicio de Auditoría de Código con LLM
Este proyecto consiste en un microservicio de análisis estático de código desarrollado sobre una arquitectura de contenedores, integrando capacidades de Inteligencia Artificial para la revisión automática de buenas prácticas.

🛠️ Tecnologías Utilizadas
Backend & Orquestación: n8n corriendo sobre Docker.

Modelo de Lenguaje (LLM): Google Gemini 2.5 Flash API.

Protocolos: HTTP Webhooks (REST API).

Infraestructura: Docker Compose.

🎯 El Problema
Como desarrolladora, buscaba una forma de automatizar la revisión de fragmentos de código (Code Snippets) en Java y .NET para detectar errores comunes o falta de estándares de Clean Code de manera inmediata, sin necesidad de configurar un servidor de integración continua (CI/CD) complejo.

💡 La Solución
Diseñé un flujo de trabajo asincrónico que:

Expone un Endpoint: Un Webhook que recibe código fuente como parámetro en una petición GET/POST.

Inyección de Contexto: Procesa el código a través de un motor de IA configurado con un perfil de Senior Software Architect.

Respuesta Sincrónica: Devuelve al cliente (navegador o app) un análisis detallado sobre posibles bugs, performance y legibilidad.

📸 Demo del Funcionamiento
<img width="1873" height="839" alt="image" src="https://github.com/user-attachments/assets/7bbc9815-351c-4c22-8df2-6f9231c8b3a4" />
<img width="1914" height="699" alt="image" src="https://github.com/user-attachments/assets/7c50c3ae-e9cd-49c4-8668-ec1ed1e914be" />



⚙️ Cómo ejecutar este proyecto
Tener instalado Docker y Docker Compose.

Configurar la variable de entorno para la API Key de Gemini.

Importar el archivo .json del workflow en n8n.

Realizar una petición al endpoint:(http://localhost:5678/webhook-test/prueba-ia?codigo=int%20x%20=%2010;)
