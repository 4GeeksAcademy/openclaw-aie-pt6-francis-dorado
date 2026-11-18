# SKILLS_DESIGN.md — Diseño de las skills de Kai

Documento escrito **antes** de implementar ninguna skill. Cada skill responde a tres preguntas: qué hace, qué input necesita y cómo es un buen output.

Restricción de partida: solo se usan las herramientas ya conectadas (Google Docs, Google Calendar y Telegram, vía Zapier MCP). Gmail, Drive, Tasks y GitHub no están conectados y no se configura ninguna conexión nueva.

---

## Skill 1: `plan-semana`

**Por qué esta tarea:** cada domingo o lunes tengo que organizar la semana a mano, y mis turnos en PRIMOR alternan entre mañana y tarde, así que el plan cambia cada semana. Es la tarea que más veces repito.

### 1. ¿Qué hace esta skill?
Convierte mis objetivos y compromisos de la semana en un plan priorizado guardado como Google Doc, y crea en Google Calendar solo los eventos clave.

### 2. ¿Qué input necesita el agente?
- **Lo que le doy:** un texto libre por Telegram con mis objetivos y compromisos de la semana, más las fechas de la semana y si es de turno de mañana o de tarde.
- **Si falta algo:** el tipo de turno o una hora/duración que cambie el resultado → pregunta una sola vez, todo junto.
- **Lo que ya sabe por los cinco archivos:** que me llamo Francisco y hablo español (`USER.md`), que mis turnos alternan por semanas, que estudio el curso de 4Geeks y quiero 1-2 horas de estudio regulares (`USER.md`), que prefiero los mensajes breves (`SOUL.md`), que debe marcar con ❓ lo no verificado (`SOUL.md`), que el calendario por defecto es el principal con zona Europe/Madrid y que no puede pasar de 5 eventos sin confirmar (`TOOLS.md` y `AGENTS.md`).

### 3. ¿Cómo es un buen output?
- **Destino:** un Google Doc titulado `Plan semanal – AAAA-MM-DD a AAAA-MM-DD`, con secciones: Prioridades (máximo 3), Agenda por día adaptada al turno, Bloques de estudio y Pendiente ❓.
- **Calendar:** como máximo 5 eventos clave, a horas que no choquen con el turno de trabajo.
- **Telegram:** mensaje de 3-5 líneas con el enlace al Doc y la lista de eventos creados.
- **Cómo sabré que funcionó:** el Doc existe con ese título, los eventos aparecen en Calendar en las horas indicadas sin pisar mi turno, y Kai ha comprobado ambas cosas antes de decir "listo".

---

## Skill 2: `diario-aprendizaje`

**Por qué esta tarea:** estoy aprendiendo mucho y se me olvida lo que no apunto. Escribir el diario cuesta más que aprender, así que quiero darle solo unos puntos sueltos y que Kai lo ordene.

### 1. ¿Qué hace esta skill?
Toma unos pocos puntos de lo que he aprendido hoy y los convierte en una entrada ordenada de diario, guardada como Google Doc, con cada punto explicado en lenguaje llano.

### 2. ¿Qué input necesita el agente?
- **Lo que le doy:** de 2 a 6 puntos sueltos por Telegram, sin formato.
- **Si falta algo:** nada obligatorio. Si no dices la fecha, usa la de hoy.
- **Lo que ya sabe por los cinco archivos:** que estudio el curso de 4Geeks y no programo pero entiendo la lógica, por lo que debe explicar con causa → efecto y sin jerga (`USER.md` y `SOUL.md`); que prefiere mensajes breves (`USER.md`); que debe marcar con ❓ lo que no ha podido verificar (`SOUL.md`); y el formato de título de los documentos `Tema – AAAA-MM-DD` (`TOOLS.md`).

### 3. ¿Cómo es un buen output?
- **Destino:** un Google Doc titulado `Diario de aprendizaje – AAAA-MM-DD`, con secciones: Lo aprendido hoy, Explicado con mis palabras, Qué me falta entender ❓ y Siguiente paso.
- **Telegram:** mensaje de 3-5 líneas con el enlace al Doc.
- **Cómo sabré que funcionó:** el Doc existe con la fecha correcta, recoge todos mis puntos sin inventar otros, el tono es llano y coherente con `SOUL.md`, y Kai lo ha comprobado antes de confirmar.

**Decisión de diseño:** una entrada = un documento nuevo, no una sola página que crece. Con la acción de crear documento, que ya está habilitada, basta; añadir texto a uno existente obligaría a activar otra acción en Zapier. Con un documento por día es fácil de archivar y no hace falta configurar nada nuevo.

---

## Por qué estas dos y no otras

- Son las que más veces activaría a la semana, y las dos usan solo Docs, Calendar y Telegram.
- Se complementan: el plan decide cuándo estudio y el diario recoge lo que he estudiado.
- Descarté las skills que necesitan Gmail, Drive, Tasks o GitHub porque no están conectados y el enunciado prohíbe configurar conexiones nuevas.
