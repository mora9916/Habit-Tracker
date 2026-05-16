# Spec: Habit Tracker

## Objetivo
Una app web para personas que quieren registrar hábitos diarios, marcar cumplimiento y ver continuidad sin gamificación ni analítica avanzada.

## Scope

### Sí entra
- Registro, login y logout con email y password.
- Crear, editar, pausar y eliminar hábitos personales.
- Cada hábito tiene nombre, descripción breve y estado activo o pausado.
- Check-in diario de hábitos activos.
- Corrección de check-ins de los últimos 7 días.
- Vista de progreso por hábito con días cumplidos y racha actual.
- Estados vacíos cuando no hay hábitos o no hay registros del día.
- Separación de datos por usuario autenticado.

### No entra
- Hábitos compartidos entre usuarios.
- Gamificación, niveles, puntos o logros.
- Analítica avanzada, reportes históricos extensos o gráficas complejas.
- Recordatorios, notificaciones o integraciones externas.
- Registro de cumplimiento futuro.
- Onboarding guiado antes de crear el primer hábito.

## Criterios de aceptación

1. Dado que una persona no tiene cuenta, cuando se registra con email y password válidos, entonces entra a la app con una sesión activa.
2. Dado que una persona ya tiene cuenta, cuando inicia sesión con credenciales válidas, entonces ve únicamente sus hábitos y registros.
3. Dado que una persona tiene sesión activa, cuando cierra sesión, entonces vuelve a la pantalla de acceso y no puede ver sus datos sin iniciar sesión otra vez.
4. Dado que el usuario no tiene hábitos, cuando entra a la app, entonces ve un estado vacío con una acción para crear su primer hábito.
5. Dado que el usuario está autenticado, cuando crea un hábito con nombre y descripción, entonces el hábito aparece en su lista como activo.
6. Dado que el usuario tiene un hábito existente, cuando edita su nombre o descripción y guarda, entonces la lista muestra los datos actualizados.
7. Dado que el usuario tiene un hábito activo, cuando lo pausa, entonces deja de aparecer como pendiente para check-in diario.
8. Dado que el usuario tiene un hábito, cuando lo elimina, entonces deja de aparecer en la lista y en la vista de progreso.
9. Dado que el usuario tiene hábitos activos, cuando marca un hábito como cumplido para hoy, entonces el hábito queda registrado como cumplido en la fecha actual.
10. Dado que el usuario marcó un hábito por error dentro de los últimos 7 días, cuando cambia el registro de esa fecha, entonces el progreso se recalcula con el nuevo dato.
11. Dado que el usuario intenta registrar una fecha futura, cuando selecciona esa fecha, entonces la app no permite guardar el check-in.
12. Dado que un hábito tiene cumplimiento consecutivo hasta hoy, cuando el usuario abre progreso, entonces ve la racha actual calculada con esos días consecutivos.
13. Dado que un hábito no fue cumplido ayer ni hoy, cuando el usuario abre progreso, entonces su racha actual se muestra como 0.
14. Dado que el usuario vuelve después de varios días sin registrar, cuando entra a la app, entonces ve sus hábitos activos pendientes para el día actual.

## No-goals
- No habrá app móvil nativa.
- No habrá modo offline.
- No habrá notificaciones push ni emails de recordatorio.
- No habrá OAuth con Google, Apple u otros proveedores.
- No habrá funciones sociales ni comparación con otros usuarios.
- No habrá diseño visual premium o sistema de marca completo.
