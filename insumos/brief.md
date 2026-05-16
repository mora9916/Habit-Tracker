# Brief: Habit Tracker

## 1. El problema

Muchas personas quieren construir hábitos diarios, pero pierden continuidad porque no tienen una forma simple de registrar avances, ver patrones y retomar cuando fallan. Las herramientas existentes suelen caer en dos extremos: listas demasiado básicas que no muestran progreso útil, o apps cargadas de gamificación, métricas y opciones que distraen del acto principal de cumplir el hábito.

El producto busca ofrecer un espacio claro para definir hábitos, marcarlos día a día y entender si la persona está sosteniendo la práctica. No pretende ser una plataforma de productividad completa, sino una herramienta enfocada para seguimiento personal durante ciclos cortos y manejables.

## 2. Núcleo obligatorio

1. Gestión de hábitos
   El usuario puede crear, editar, pausar y eliminar hábitos que quiere seguir. Cada hábito debe tener la información mínima necesaria para reconocerlo y decidir cuándo cuenta como cumplido.
   Decisiones abiertas: ¿Los hábitos serán siempre diarios o podrán tener frecuencias distintas? ¿Qué significa pausar un hábito frente a eliminarlo?

2. Registro diario de cumplimiento
   El usuario puede marcar si cumplió o no cada hábito en una fecha determinada. La experiencia principal debe permitir registrar el día actual con poco esfuerzo y corregir días recientes si se equivocó.
   Decisiones abiertas: ¿Se permite registrar cumplimiento futuro? ¿Qué rango de fechas pasadas se puede editar?

3. Vista de progreso
   El usuario puede ver una síntesis del avance de sus hábitos: días cumplidos, continuidad reciente y señales básicas de consistencia. La vista debe ayudar a entender el comportamiento sin convertir el producto en analítica avanzada.
   Decisiones abiertas: ¿Qué métrica principal representa mejor el progreso: racha, porcentaje, calendario o una combinación simple?

4. Cuenta y datos personales
   El usuario puede iniciar sesión y conservar sus hábitos y registros asociados a su cuenta. La app debe separar claramente los datos de cada usuario.
   Decisiones abiertas: ¿El producto requiere onboarding inicial o basta con entrar directo a crear el primer hábito?

5. Estado vacío y recuperación de uso
   La app debe guiar al usuario cuando todavía no tiene hábitos, cuando no ha registrado el día o cuando vuelve después de varios días sin usarla. Estos estados forman parte del flujo principal, no son detalles decorativos.

## 3. Extensiones (elegir máximo 1)

| Extensión | Descripción |
|---|---|
| Recordatorios | Configurar avisos simples para hábitos en horarios elegidos por el usuario. |
| Categorías | Agrupar hábitos por áreas como salud, estudio, trabajo o bienestar. |
| Notas diarias | Añadir una nota breve por día para explicar contexto, obstáculos o aprendizajes. |
| Objetivos por periodo | Definir metas semanales o mensuales para hábitos que no requieren cumplimiento diario perfecto. |
| Compartir progreso | Generar una vista o resumen compartible de avance sin exponer datos sensibles. |
| Plantillas de hábitos | Ofrecer hábitos sugeridos para crear rápidamente una rutina inicial. |

## 4. Restricciones técnicas

- Proyecto web con Next.js 15 y App Router.
- Supabase para Postgres y Auth.
- Deploy en Vercel.
- TypeScript estricto.
- Tailwind para estilos.
- Alcance pensado para 2-3 semanas de trabajo enfocado por un developer con experiencia básica dirigiendo agentes de IA.

## 5. Lo que NO se evalúa

- Diseño visual premium o sistema de marca completo.
- Performance avanzada más allá de una experiencia razonable para uso personal.
- Tests automatizados exhaustivos.
- Responsive perfecto en todos los tamaños y dispositivos.
- Funciones comerciales como pagos, planes, equipos, marketplace o integraciones externas complejas.
