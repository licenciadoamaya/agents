# Definción de arquitectura sobre cloudflare
---

**Worker normal:**
Crea e implementa funciones, sitios web y aplicaciones full-stack sin servidor.

**Containers:**
Permite la ejecución de contenedores serverless.
Uso: https://developers.cloudflare.com/containers/index.md
* Solo se usa si la indicación es explicitamente usar containers 

**Cloudflare Workers:**
Arquitectura sin cold starts que pemite manejar logicas sobre V8 y también renderizado dinamico sobre http con SSR, alojamiento de servidores y otras funciones importantes.
*Ejemplo*: Si tengo que crear una integración API, uso un worker con un framework como hono que se encargue de manejar la API.

**Workers AI:** 
Se encarga de procesar imagenes y es uno de los modelos mas importantes que permiten acceder a modelos de vanguardia, estos se usan si te pido integración con IA para no salir a usar APIs externas a cloudflare nos conectamos usando estos workers.
*Ejemplo*: Tengo que procesar mas de 200 imagenes y extraer información entonces uso el worker ai para enviar las imagenes 1 a 1 y luego recibir la informacion que requiero.

**KV:** 
Usado para almacenas datos que no cambian constantemente, un ejemplo es el perfil o configuración de un usuario.

**D1 Database:**
Usada para almacenar los datos de manera estructurada y asi poder facilitar el acceso a los mismos siempre respetando indices, relaciones y llaves foraneas.

**Hyperdrive:**
Permite la integración de bases de datos postgree y mysql externas.

**R2 Storage:**
Permite un correcto manejo de integraciiones con almacenamiento de archivos.

**Argo Smart Routing:**
Sirve para acelerar la entrega y permitir que el usuario haga uso de la red de cloudflare.

**Stale-While-Revalidate:**
Implementa el contenido antiguo mientras se actualiza la versión mas nueva en mi servidor. 

**WAF:** 
Bloquea exploit conocidos de manera automática

**Turnstile:** 
Reemplaza captchas invisibles para seguridad de los usuarios.

**Bot management:** 
Mitigrar el scraping y ataques de relleno de credenciales

**Polish y Mirage:** 
Procesamiento de contenido multimedia y conversión, normalmente no se usa porque me genera costos adicionales.

**Auto minify:**
Minifica automáticamente todos los assets.

**Basin de cloudflare:**
Usado para almacenamientod de eventos en sqls distribuidos.

**Rocket loader**: 
Carga correctamente los scripts de javascript

**Observability:**
Estos eventos necesito almacenarlos todos porque son demasiado y me generan costo, solo eventos criticos puedo almacenar.

**Durable Objects:**
Crea aplicaciones colaborativas, chats en tiempo real, juegos multijugador y mucho más sin necesidad de coordinar el estado ni gestionar la infraestructura.
Documentación: https://developers.cloudflare.com/durable-objects/index.md

**Qeues:**
Cloudflare Queues is a flexible messaging queue that allows you to queue messages for asynchronous processing. By following this guide, you will create your first queue, a Worker to publish messages to that queue, and a consumer Worker to consume messages from that queue.



**Workflows:**
Build durable multi-step applications on Cloudflare Workers with Workflows.



**Browser Run:**
Run headless Chrome on Cloudflare's global network for browser automation, web scraping, testing, and content generation.



**Workers VPC:**
Securely connect your private cloud to Cloudflare to build cross-cloud apps.
Workers VPC allows you to connect your Workers to your private APIs, services, and databases in external clouds (AWS, Azure, GCP, on-premise, and others) that are not accessible from the public Internet.


**Email Sending:**
Send your first email using the Workers binding, the REST API, or SMTP.


**Email Routing:**
Set up email routing to forward incoming emails to existing mailboxes or process them with Workers.


**Flagship:**
Ship features safely with feature flags.

## Storage: 
Artifacts: Almacenamiento de archivos compatible con Git para agentes de IA. Permite enviar, clonar, crear ramas y comparar con cualquier cliente Git estándar.

Analytics Engine: 
Obtén rápidamente información analítica adicional importante para tus workers.

Basin Catalog:
Managed Apache Iceberg catalog with automated table maintenance - Turn your R2 bucket into a managed data lake.

Basin Pipelines:
Ingest, transform, and load streaming data into Iceberg or Parquet in R2.

Streams:
Manage streaming data sources for your pipelines.

Sinks:
Manage data destinations for your pipelines.

K2 Streams:
Create and manage durable streams for your event data.

Secrets Store:
Encrypt and store sensitive information as secrets that are securely reusable across an account.

Realtime:
Crea aplicaciones de vídeo y audio en tiempo real con Cloudflare RealtimeKit.

## AI 
- Models: Modelos existentes en cloudflare.
Documentación: https://developers.cloudflare.com/workers-ai/models/index.md

- AI Gateway: Evita estar conectando multiples APIS
- MCP Portals: Create a single endpoint for multiple MCP (Model Context Protocol) servers. Server portals help to streamline visibility and security of your AI infrastructure.
- Vectorize: Crea aplicaciones de IA completas con Vectorize, la potente base de datos vectorial de Cloudflare. Combínala con Workers AI para almacenar y consultar incrustaciones, o bien, integra tus propias incrustaciones en Vectorize.
- AI Search: Crea experiencias de búsqueda basadas en inteligencia artificial con tus datos para ofrecer respuestas en lenguaje natural en tus aplicaciones.
- Agent tracing: El seguimiento de agentes le ayuda a comprender qué hizo un agente en cada paso del proceso, incluyendo sus llamadas a modelos, ejecuciones de herramientas y solicitudes de aprobación. Utilice los seguimientos para investigar comportamientos inesperados, detectar operaciones lentas y revisar el uso de tokens.
