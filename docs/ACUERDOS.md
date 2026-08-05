# Acuerdos de trabajo y dinámica del equipo

## Metodología
Trabajaremos bajo una adaptación ágil inspirada en **Scrum**, dividiendo el proyecto en 4 iteraciones semanales (Sprints). La dedicación estimada será de 3 horas minimas por semana por integrante.

## Flujo de Trabajo (Git Workflow)
1. El repositorio principal está alojado en GitHub.
2. Nadie hace *commits* directos a la rama `main`.
3. Se utilizarán ramas independientes para cada funcionalidad con la nomenclatura: `feature/nombre-de-la-tarea` (ej. `feature/login`, `feature/expense-form`).
4. Para integrar código a `main`, se creará un **Pull Request (PR)**.
5. Al menos un integrante distinto al autor debe aprobar el PR antes de hacer *merge* para evitar conflictos y asegurar la calidad del código.

## Independencia técnica
Para no bloquear el trabajo de los demás, el equipo acuerda definir estructuras de datos simuladas (Mocks) en la primera semana. De esta forma, el desarrollo de la Interfaz (UI) y la lógica de estado pueden avanzar en paralelo.

## Reuniones
Se realizará al menos una reunión semanal de sincronización (Durante las clases) para planificar las tareas de la semana, evaluar el progreso y resolver posibles bloqueos. Las comunicaciones asíncronas se manejarán vía [Discord].