# 📖 Guía de trabajo gitFlow (Wallet App)

## 1. Estándar de ramas

El proyecto utilizará un flujo de trabajo basado en dos ramas principales y ramas temporales para el desarrollo.

### 🌿 Ramas principales

#### `main` (Producción)
- Contiene el código estable y funcional.
- Vercel realizará el despliegue automático desde esta rama.
- **No se permiten commits directos.**

#### `develop` (Integración)
- Rama donde se integran todas las funcionalidades.
- Se utiliza para validar el funcionamiento conjunto antes de pasar a producción.

### 🌱 Ramas de trabajo (Temporales)

Toda nueva tarea debe crearse desde `develop` utilizando los siguientes prefijos:

- `feature/nombre-tarea` → Nuevas funcionalidades.
  - Ejemplo: `feature/login`
  - Ejemplo: `feature/formulario-gastos`

- `fix/nombre-bug` → Corrección de errores.
  - Ejemplo: `fix/calculo-balance`

- `chore/nombre-tarea` → Configuración o mantenimiento.
  - Ejemplo: `chore/instalar-zod`

---

## 2. Flujo de trabajo diario

### Paso 1. Sincronizar el entorno local

Siempre obtén la última versión antes de comenzar.

```bash
git checkout develop
git pull origin develop
```

### Paso 2. Crear la rama de trabajo

```bash
git checkout -b feature/mi-nueva-tarea
```

### Paso 3. Desarrollar y realizar commits

Utiliza commits pequeños y descriptivos.

Convenciones:

- `feat:` Nueva funcionalidad.
- `fix:` Corrección de errores.
- `style:` Cambios de estilos (CSS/Tailwind).

```bash
git add .
git commit -m "feat: agregar validación de montos con zod"
```

### Paso 4. Subir la rama y crear el Pull Request

```bash
git push origin feature/mi-nueva-tarea
```

Luego:

- Crear un Pull Request en GitHub.
- La rama destino debe ser **`develop`**.
- **Nunca abrir un PR hacia `main`.**

### Paso 5. Revisión y Merge

- Asignar un compañero como revisor.
- Revisar el código.
- Aprobar el Pull Request.
- Realizar el Merge hacia `develop`.
- Eliminar la rama temporal.

### Paso 6. Pase a Producción

Al finalizar el sprint:

- Crear un Pull Request de `develop` hacia `main`.
- Aprobar el PR.
- Vercel desplegará automáticamente la aplicación.

## ✅ Equipo

Antes de la entrega final:

- Revisar que el CI/CD de Vercel funcione correctamente.
- Verificar que no existan errores en el despliegue.
- Actualizar y completar el `README.md`.
- Preparar la entrega final del proyecto.