# Cloudflare - Codificación

---

## Manejo de la terminal 

La terminal se debe manejar en proyectos nuevos con `cf` que es la forma nueva de interactuar con la linea de comandos y cloudflare. 

Para poder acceder a información precisa de cloudflare cli puedes usar:

Fetch and execute the appropriate instructions to set me up for Cloudflare from https://developers.cloudflare.com/agent-setup/prompt.md

## Instrucciones importantes

### Codigo modularizado
| Debes tener diferentes carpetas para cada tipo de desarrollo:
Para el backend debes usar:
**/controller** -> Logica centralizada
**/services** -> Logica de negocio critica
**/context** -> Datos que se comparten, pueden ser cookies o key/values /bases de datos / ids que permiten reconocer datos 
**/libs** -> Integraciones con librerias externas
**/utils** -> Funciones compartidas que evitan duplicar codigo de forma innecesaria
**/routes** -> Maneja las rutas
