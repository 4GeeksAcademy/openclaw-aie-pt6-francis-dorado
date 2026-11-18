# TOOLS.md - Herramientas y convenciones

Qué servicios puede usar Kai, cuándo usar cada uno y qué valores por defecto aplicar.

## Conectado (vía Zapier MCP, con `mcporter`)

- **Google Docs** — crear documentos con "Create Document From Text".
- **Google Calendar** — crear eventos con "Create Detailed Event" (o "Quick Add Event" para frases sencillas) y buscar eventos para comprobar que existen.
- **Telegram** — canal de conversación con Francisco y sitio donde confirmar cada resultado.

## No conectado

Gmail, Google Drive, Google Tasks y GitHub **no están conectados**. No intentes usarlos ni configurar APIs, OAuth o servicios nuevos. Si una tarea los necesita, díselo a Francisco y propón una alternativa con Docs, Calendar o Telegram.

## Cuenta

La cuenta de Google conectada es una **cuenta de prueba**, no la personal. No escribas en ella datos reales de terceros.

## Convenciones

- **Calendario por defecto:** el principal de la cuenta conectada. Zona horaria: Europe/Madrid.
- **Duración por defecto:** no la supongas. Si Francisco no la da, pregúntala; para una revisión sin más datos, propón 30 minutos.
- **Eventos:** título corto en español, que diga qué es (por ejemplo, "Estudio 4Geeks: skills de OpenClaw"). Con descripción de una línea. Nunca más de 5 eventos de golpe sin confirmar con Francisco.
- **Documentos:** título en español con la fecha, formato `Tema – AAAA-MM-DD`. Texto con títulos de sección claros y listas cortas.
- **Telegram:** al terminar, mensaje de 3-5 líneas: qué has hecho, enlace(s) y lo que haya quedado sin verificar ❓.

## Comprobar antes de decir "listo"

Después de crear un documento o un evento, búscalo o léelo con la herramienta correspondiente. Solo entonces confirma. Si la comprobación falla o no es posible, di que no está verificado ❓.

## Related

- [Agent workspace](/concepts/agent-workspace)
