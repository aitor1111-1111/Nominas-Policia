# Mi Alquiler

PWA local para gestionar inquilinos, alquileres, facturas y liquidaciones.

## Publicación en GitHub Pages

Sube el contenido de esta carpeta a la raíz del repositorio `Mi-Alquiler` y configura GitHub Pages para desplegar desde la rama principal y la carpeta raíz. El archivo de entrada es `index.html`.

## Actualización sin perder los datos locales

Esta versión conserva el mismo nombre de base de datos IndexedDB (`mi-alquiler-db`), almacén (`records`) y clave (`main`) que las versiones anteriores. Al actualizar los archivos en la misma URL/origen y abrir la aplicación en el mismo navegador y dispositivo, la aplicación lee los datos existentes; no borra ni reinicializa la base de datos que ya contiene inquilinos y facturas.

**Antes de actualizar:** abre la versión actual en el móvil y entra en «Copias» para descargar una copia JSON de seguridad. La copia incluye los documentos adjuntos codificados dentro del JSON. Guárdala fuera del navegador.

No borres los datos del sitio, no desinstales la PWA y no cambies la URL del repositorio durante la actualización. Si se abre en otro navegador, dispositivo o dirección web, los datos locales no se comparten automáticamente.

## Reglas de liquidación

- Agua: reparto diario entre inquilinos con ocupación efectiva; los días de ausencia temporal no se imputan.
- Residuos: reparto diario entre inquilinos con contrato vigente; la ausencia temporal no exime de esta partida.
- Baja definitiva: deja de participar desde la fecha de salida registrada.
- Internet: 5 euros por persona y mes, prorrateados por días de ocupación efectiva.
- Alquiler: permanece según contrato durante una ausencia temporal.
- Las facturas marcadas como pagadas se excluyen de las liquidaciones.

La factura de Mancomunidad AG2026555311 se incorpora desglosada: agua 67,68 € (IVA incluido), del 09/06/2026 al 08/10/2026; residuos 61,15 € (IVA incluido), del 01/09/2026 al 31/12/2026. PDF original incluido.

## Almacenamiento y privacidad

Los datos se guardan en IndexedDB del navegador. No hay sincronización automática entre dispositivos ni envío a un servidor. Mantén copias de seguridad periódicas, especialmente antes de actualizar el navegador o cambiar de móvil.


## Consulta de facturas con ChatGPT (opción manual asistida)

En la pestaña Facturas, el botón «Consultar Outlook con ChatGPT» abre ChatGPT y copia una instrucción para buscar correos de BASER y Mancomunidad mediante la conexión de Outlook disponible en ChatGPT. El usuario debe pegar y enviar la instrucción en ChatGPT, revisar los resultados y copiar el contenido del correo a Mi Alquiler para analizarlo. Este botón no conecta la PWA directamente con Outlook, no ejecuta consultas en segundo plano y no guarda facturas automáticamente.
