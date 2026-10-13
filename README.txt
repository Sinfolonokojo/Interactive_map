EL CUIDADO QUE NAVEGA — VERCEL

1. Extrae todo el ZIP.
2. Crea un repositorio en GitHub y sube el contenido de el-cuidado-vercel:
   vercel.json, README.txt y la carpeta public con index.html dentro.
   vercel.json debe quedar en la raíz del repositorio.
3. En Vercel: Add New > Project > importa ese repositorio.
4. Framework Preset: Other. Root Directory: raíz del repositorio.
   Sin comando de instalación ni de compilación.
   Output Directory: public (ya definido en vercel.json).
5. Pulsa Deploy y comparte la URL HTTPS que entregue Vercel.

No requiere Node, Python, localhost ni claves API para los visitantes.
Se necesita internet para el mapa, las fuentes y las actualizaciones.
Este paquete está preparado para desplegar; aún no está publicado en Vercel.

ACTUALIZACIÓN DE LAS RESPUESTAS

Conectado a la pestaña "Respuestas de formulario 1" de:
https://docs.google.com/spreadsheets/d/1dEPWo67stK4qTJL7747GTolYOjBhnAIgIbMcvqVTrFk/edit

Al abrir la página se consulta Google Sheets y después cada 60 segundos
mientras la página esté abierta. Google puede tardar en reflejar los cambios
y el navegador puede retrasar las consultas de pestañas en segundo plano.
No necesitas volver a desplegar cuando llegan nuevas respuestas.
El pie indica "Hoja en vivo" y la hora de la última lectura correcta.

Primero consulta solo los títulos de las preguntas; después solicita solo
las columnas utilizadas en el mapa. Reconoce las preguntas por su texto,
sin depender de su posición. No descarga la columna de correo o WhatsApp.
Solo muestra respuestas con consentimiento "Sí, acepto".
No renombres la pestaña ni cambies las preguntas sin actualizar la configuración.

Si falla Google, conserva la última lectura correcta de esa sesión. Si no
ha logrado conectarse, muestra las 12 respuestas del CSV de respaldo original.
Cuando vuelve la conexión, reintenta automáticamente.

PRIVACIDAD

La hoja enlazada permite lectura pública. El filtro del mapa NO protege
las columnas de la hoja original: alguien con el enlace podría verlas.
Antes de difundir el sitio, usa una hoja separada que excluya correos,
teléfonos y contactos. Mantén privada la hoja original de respuestas.
Para cambiar de hoja, edita SHEET_ID y SHEET_NAME en public/index.html.
La nueva hoja necesita permitir lectura pública; verifica que aparezca
"Hoja en vivo". También se puede configurar CSV_URL con un CSV publicado
que contenga únicamente las columnas depuradas.

SI NO CARGA

- Error 404 de Vercel: comprueba public/index.html y Output Directory public.
- Solo aparece respaldo: revisa el acceso público y el nombre de la pestaña.
- Error 403 en mosaicos: usa la URL HTTPS de Vercel; no abras index.html
  directamente. Si persiste, revisa las restricciones de red/navegador y
  la política del proveedor. El contorno y las historias siguen disponibles.

Documentación:
https://vercel.com/docs/builds/configure-a-build
https://developers.google.com/chart/interactive/docs/spreadsheets
https://operations.osmfoundation.org/policies/tiles/
