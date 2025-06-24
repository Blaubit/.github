# 🧭 Guía para contribuir

Gracias por contribuir a los proyectos de **Blaubit** 🚀

---

## 🚀 ¿Cómo contribuir?

1. Creá una rama descriptiva (ej: `feature/login-endpoint`).
2. Hacé tus cambios y asegurate de seguir los estándares.
3. Verificá que el código funcione correctamente (tests si aplica).
4. Abrí un Pull Request mencionando el issue relacionado (`Closes #X`).

---

## 📐 Estándares de código (TypeScript/JavaScript)

### 📛 Nomenclatura

- **Clases, Interfaces, Tipos, Enums:** `PascalCase` → `UserService`, `PaymentGateway`
- **Variables y funciones:** `camelCase` → `getUserById`, `currentDate`
- **Constantes:** `MAYÚSCULAS_CON_SNAKE_CASE` → `MAX_RETRIES`, `API_TIMEOUT`
- **Archivos:**
  - Clases o módulos principales: `PascalCase` → `UserController.ts`
  - Helpers y utilidades: `camelCase` → `dateUtils.ts`
  - Tests: Mismo nombre que el archivo fuente + `.test.ts` → `UserService.test.ts`

### 🎨 Estilo de código

- Usar **punto y coma** al final de cada declaración
- **Comillas simples** para strings (excepto JSX)
- Indentación de **2 espacios**, no tabs
- Llaves de apertura en la **misma línea**
- Espacios adecuados (`const sum = a + b;`)
- Imports organizados en 3 bloques:

```ts
// 1. Librerías externas
import express from "express";
import cors from "cors";

// 2. Utilidades internas
import { formatDate } from "../../utils/dateUtils";

// 3. Módulos locales
import AppointmentController from "./AppointmentController";
```

---

## 🏗️ Estructura de archivos

### Estructura de Archivos (Backend con Express)

```
/src
  /config         # Configuración: base de datos, variables de entorno
  /controllers    # Controladores de endpoints
  /migrations     # Archivos de migración Sequelize
  /models         # Modelos Sequelize (estructuras de tablas)
  /routes         # Rutas de Express (entry points)
  /services       # Lógica de negocio desacoplada del controlador
  /utils          # Funciones auxiliares (helpers)
  index.ts        # Punto de entrada principal
```

---

## 🧪 Testing

- Usar `describe` e `it` con nombres claros
- Seguir patrón AAA:
  - **Arrange** (preparación)
  - **Act** (ejecución)
  - **Assert** (verificación)

---

## 📝 Documentación

- Documentar endpoints con Swagger (OpenAPI)
- Si agregás nuevos servicios o modelos, actualizá las referencias internas
- Comentarios breves pero útiles, evitar redundancias

---
 
## 🔄 Git

- Usar mensajes de commit en presente (español):
  - ✅ Correcto: `feat: agrega formateador prettier`  
  - ❌ Incorrecto: `agregué formateador prettier`  
  - ✅ Correcto: `fix: corrige validación de formulario`
  - ❌ Incorrecto: `corregí el bug del formulario`

**Convención**:  
`<tipo>: <mensaje breve en presente>`

### Prefijos recomendados (Tipos):

- `feat`: Nueva funcionalidad
- `fix`: Corrección de errores
- `docs`: Solo documentación
- `refactor`: Mejora interna sin cambio funcional
- `test`: Cambios o adición de tests
- `chore`: Mantenimiento, configuración, scripts

---

## 💡 Recomendaciones finales

- Validar entradas de usuario y reglas claras
- Manejar errores con `try/catch`, logs o middlewares
- Dividir funcionalidades en pequeños servicios reutilizables
- Pensar en escalabilidad y claridad del código

---

💙 ¡Gracias por mantener la calidad y profesionalismo del proyecto!
