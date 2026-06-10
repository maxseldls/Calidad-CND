Guía: Reporte Calidad CND
1. Requisitos previos
Instalar una sola vez:

Python 3.10+

Descargar desde python.org/downloads — marcar "Add to PATH" al instalar
Dependencias Python (abrir terminal/cmd en la carpeta del proyecto):


pip install python-pptx openpyxl requests
Claude Code (la app que ejecuta el script):

Descargar desde claude.ai/download o instalar la extensión en VS Code
Necesita cuenta Claude (Pro o Team)
2. Estructura de carpetas
Colocar los archivos en esta estructura exacta:


C:\PROYECTOS NINJISTICOS\CALIDAD CND\
├── montar_reporte.py
├── PLANTILLA\
│   └── CND - Informe Calidad - Plantilla.pptx
└── DATA\
Si quieres usar otra ruta, avísame — hay que ajustar las constantes en el script.

3. Cada semana, hacer esto
Paso 1 — Preparar el Excel de data

Guardar el Excel de quejas como:


DATA\Reporte_Calidad_<rango>.xlsx
Ejemplo: DATA\Reporte_Calidad_CND_03_10Jun_2026.xlsx

El Excel debe tener:

Hoja Resumen: columnas Temática, # Menciones, % Negativo, % Neutral, Resumen
Una hoja por cada temática con título formato "Nombre • N menciones"
Paso 2 — Abrir Claude Code en la carpeta del proyecto

En VS Code: abrir la carpeta CALIDAD CND → panel de Claude Code (icono en barra lateral)

Paso 3 — Dar el prompt

Simplemente escribir algo como:

Montar el reporte de calidad CND del 3 al 10 de junio de 2026. El Excel está en DATA/Reporte_Calidad_CND_03_10Jun_2026.xlsx.

Claude va a:

Leer el Excel
Generar los hallazgos automáticamente
Ejecutar montar_reporte.py
Dejar el PPT terminado en PLANTILLA/CND - Informe Calidad - 03-10Jun2026.pptx
4. Credencial Brandwatch (para los slides de Residuos Sólidos y Reforma Fiscal)
El script usa una API key de Brandwatch. Compartirte la clave por separado — agregarla como variable de entorno o indicarla cuando Claude lo pida.

5. Si algo falla
"La plantilla está abierta" → cerrar PowerPoint y volver a intentar
Error de permisos Python → correr la terminal como administrador
Chart no se actualiza bien → avisar, el script tiene un paso de patch automático pero a veces requiere ajuste manual mínimo
