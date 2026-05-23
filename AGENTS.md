# AGENTS.md — Contrato del proyecto

Este archivo rige a todos los agentes custom y developers humanos que trabajen en Habit Tracker.
Si una instrucción local contradice este contrato, prevalece este contrato salvo plan aprobado.

## Stack

- Next.js 15 con App Router.
- Supabase: Postgres, Auth y Storage.
- Deploy en Vercel.
- TypeScript en modo estricto.
- Tailwind CSS para estilos.
- La app sigue `spec.md`; no ampliar alcance sin plan aprobado.

## Convenciones de TypeScript

- Mantener `strict` activo y resolver errores de tipos antes de cerrar una unidad.
- Tipar explícitamente props, retornos públicos, payloads de Supabase y respuestas de acciones.
- Prohibido usar `any` sin justificación escrita en el plan o en el comentario mínimo del cambio.
- Preferir `unknown` + narrowing, tipos derivados y enums/unions claras antes que casts amplios.
- Validar datos en cliente y servidor cuando crucen formularios, rutas, Supabase o Stripe.
- Usar nombres descriptivos en español o inglés consistente; no abreviaturas opacas.

## Estructura Esperada

- `src/app`: rutas, layouts y páginas del App Router.
- `src/components`: componentes reutilizables sin lógica de dominio pesada.
- `src/features`: módulos por dominio cuando una función agrupe UI, hooks y lógica.
- `src/lib`: clientes, helpers compartidos, tipos base y utilidades de integración.
- `supabase/migrations`: migraciones versionadas de base de datos y RLS.
- Documentación raíz: `README.md`, `spec.md`, `CONTEXT.md`, `AGENTS.md`.
- Se puede ajustar organización interna si conserva límites claros y no contradice `spec.md`.

## Política de Commits

- No se escribe código sin plan aprobado.
- Cada commit debe ser atómico, verificable y corresponder a una unidad funcional.
- Prohibidos commits tipo "implement everything" o mezclas de cambios no relacionados.
- Antes de commitear, revisar `git status` y validar solo lo necesario para la unidad.
- Todo cambio terminado debe quedar versionado; nada aprobado queda suelto sin commit.

## Flujo Git

- `main` es estable y solo recibe integraciones ya validadas.
- `develop` es la rama de integración.
- Cada unidad de trabajo usa una rama tipada desde `develop`: `feat/`, `docs/`, `chore/` o `fix/`.
- Las ramas tipadas se integran de vuelta a `develop`.
- No borrar ni reescribir commits existentes sin instrucción explícita y plan aprobado.

## Regla de CONTEXT.md

- Toda edición manual de código no generada por un agente debe documentarse en `CONTEXT.md`.
- La entrada debe explicar qué se editó, por qué fue manual y qué riesgo o decisión cubre.
- Cambios generados por agente no requieren entrada en `CONTEXT.md` salvo que el plan lo pida.

## Prohibiciones Explícitas

- Prohibido usar `any` sin justificación.
- Prohibido incorporar librerías pesadas de componentes como Material UI o Chakra.
- Prohibido agregar tests automatizados para este alcance.
- Prohibido escribir código, migraciones o configuración sin plan aprobado.
- Prohibido cambiar el stack, el modelo de planes, los no-goals o el alcance de `spec.md` sin nuevo plan.

## Autonomía Permitida

- Agentes pueden decidir nombres internos, extracción de helpers y composición local de componentes.
- Agentes pueden ajustar detalles menores de Tailwind respetando una UI sobria y consistente.
- Agentes pueden proponer archivos dentro de la estructura esperada si reducen complejidad real.
- Están cerrados por contrato: stack, gitflow, alcance de `spec.md`, ausencia de tests automatizados y límites Free/Premium.
