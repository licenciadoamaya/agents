# Cloudflare - Codificación Frontend

---

## Instrucciones importantes

### Codigo modularizado
| Debes tener diferentes carpetas para cada tipo de desarrollo:
Para el backend debes usar:
**/services** -> Logica de negocio critica.
**/context** -> Datos que se comparten para evitar sobre anidamiento de variables entre componentes, preferible usar zustand o alternativas parecidas. 
**/libs** -> Integraciones con librerias externas pero facilitando el control y ensamble de las mismas.
**/utils** -> Funciones compartidas que evitan duplicar codigo de forma innecesaria
**/routes** -> Maneja las rutas que permiten asociarlas a paginas y son dinamicas o estaticas

### Librerias importantes
- tailwindcss: usada para facilitar el manejo de css y evitar sobrecargar con css innecesario
- shadcn: Evitar crear componentes individuales y usar estos componentes en su lugar
- zustand: en cliente para facilitar el compartir datos

