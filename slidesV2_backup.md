---
theme: default
background: https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1920&q=60
title: CRUD con Spring Boot y JPA
info: |
  Curso práctico de Spring Boot con JPA/Hibernate
  para desarrolladores con conocimientos en Java.
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
---

# CRUD con Spring Boot y JPA

<div class="text-xl text-gray-300 mt-2">
Spring Boot · JPA · Hibernate · REST · Postman
</div>

<div class="pt-8 text-gray-400 text-sm">
  Nivel Intermedio · Requiere conocimientos en Java
</div>

---

# ¿Qué es Vibe Coding?

**Vibe Coding** es una forma de programar donde el desarrollador describe en lenguaje natural lo que quiere construir y una IA genera el código automáticamente.

El término fue acuñado por **Andrej Karpathy** en 2025 y describe el cambio de paradigma donde el foco pasa de escribir código a **dirigir, revisar y validar** lo que la IA produce.

### Idea central

> "No escribes el código, describes lo que quieres y la IA lo construye. Tú eres el arquitecto, la IA es el constructor."

---

# Vibe Coding — ¿Cómo funciona?

<v-clicks>

1. 🧠 **Describes** lo que necesitas en lenguaje natural
2. 🤖 **La IA genera** el código, los archivos o la estructura
3. 👀 **Revisas** el resultado y validas que sea correcto
4. 🔁 **Iteras** con más instrucciones si algo no está bien
5. ✅ **Apruebas** y el código queda integrado al proyecto

</v-clicks>

---

# Vibe Coding — Ventajas y Consideraciones

### Ventajas

| Ventaja | Descripción |
|---------|-------------|
| ⚡ Velocidad | Genera código en segundos que tomaría minutos o más |
| 🎯 Foco | El desarrollador se concentra en arquitectura y decisiones |
| 📚 Aprendizaje | Ver el código generado ayuda a entender nuevos conceptos |
| 🔁 Iteración rápida | Probar ideas sin invertir tiempo en implementación |

### Consideraciones

- No reemplaza entender el código — debes poder revisarlo y corregirlo
- La calidad del resultado depende directamente de la calidad de la instrucción
- Siempre validar seguridad, rendimiento y buenas prácticas en el código generado

---

# IDEs con IA Integrada

Los entornos de desarrollo modernos ya incluyen asistentes de IA directamente en el editor.

| IDE | IA integrada | Característica destacada |
|-----|-------------|--------------------------|
| **Kiro** | IA agéntica propia | Spec, steering, hooks, agentes autónomos |
| **Cursor** | GPT-4 / Claude | Chat con el codebase completo |
| **GitHub Copilot** | OpenAI Codex | Autocompletado en tiempo real |
| **IntelliJ IDEA** | AI Assistant | Integración nativa con el ecosistema JetBrains |
| **VS Code** | Copilot / extensiones | Amplio ecosistema de extensiones de IA |

---

# Kiro IDE

**Kiro** es un IDE agéntico construido sobre VS Code que va más allá del autocompletado: puede planear, diseñar e implementar funcionalidades completas de forma autónoma.

### Conceptos clave de Kiro

| Concepto | Descripción |
|----------|-------------|
| **Spec** | Flujo estructurado: requisitos → diseño → tareas → implementación |
| **Steering** | Archivos `.md` que le dan contexto y reglas permanentes al agente |
| **Hooks** | Automatizaciones que se ejecutan en eventos del IDE |
| **Autopilot** | Modo autónomo: Kiro trabaja de extremo a extremo sin interrupciones |
| **Supervised** | Modo supervisado: aprueba cada cambio antes de que se aplique |

---

# ¿Qué es Prompt Engineering?

**Prompt Engineering** es la práctica de diseñar y redactar instrucciones claras y efectivas para obtener los mejores resultados de un modelo de IA.

### ¿Por qué importa?

> La calidad del output de la IA es directamente proporcional a la calidad del input que le das.

Una instrucción vaga produce resultados vagos. Una instrucción precisa produce resultados precisos.

---

# Prompt Engineering — Conceptos Básicos

<v-clicks>

- 🎯 **Contexto** — darle a la IA información sobre el proyecto, tecnología y objetivo
- 📋 **Rol** — indicarle cómo debe comportarse: *"actúa como un desarrollador Java senior"*
- 🔍 **Especificidad** — ser concreto en lo que se pide, evitar ambigüedades
- 📐 **Formato** — indicar cómo quieres la respuesta: lista, tabla, código, explicación
- 🔁 **Iteración** — refinar el prompt si el resultado no es el esperado

</v-clicks>

---

# Prompt Engineering — Buenas Prácticas

### Prompt débil
```
"Hazme un CRUD en Java"
```

### Prompt efectivo
```
"Crea un CRUD REST con Spring Boot 3.2 y JPA para la entidad Curso
con los campos: id, nombre, descripcion, precio y activo.
Usa la arquitectura Controller-Service-Repository.
Incluye manejo de excepciones con @RestControllerAdvice
y validaciones con @Valid. La base de datos es MySQL."
```

### Diferencia clave
El prompt efectivo incluye: **tecnología**, **versión**, **entidad**, **campos**, **arquitectura** y **requisitos adicionales**.

---

# Tipos de Prompts más usados en Desarrollo

| Tipo | Ejemplo |
|------|---------|
| **Generación** | "Crea una clase Java que represente un Curso con JPA" |
| **Explicación** | "Explícame qué hace la anotación @Transactional" |
| **Refactoring** | "Refactoriza este Service para aplicar el principio de responsabilidad única" |
| **Depuración** | "Tengo este error al arrancar Spring Boot, ¿cuál es la causa?" |
| **Completado** | "Completa los métodos que faltan en este Repository" |
| **Revisión** | "Revisa este código y sugiere mejoras de seguridad y rendimiento" |

---

# ¿Qué es Spring Boot?

Spring Boot es un framework basado en Spring que permite crear aplicaciones Java de forma rápida, con configuración mínima.

### Ventajas principales

<v-clicks>

- 🚀 **Autoconfiguración** — detecta dependencias y configura automáticamente
- 📦 **Servidor embebido** — incluye Tomcat, no necesitas desplegarlo externamente
- 🔧 **Sin XML** — configuración por anotaciones y propiedades
- ⚡ **Arranque rápido** — proyecto funcional en minutos

</v-clicks>

---

# Inversión de Control e Inyección de Dependencias

### Inversión de Control (IoC)
Spring gestiona la creación y el ciclo de vida de los objetos. El desarrollador no instancia clases manualmente, Spring lo hace por ti.

### Inyección de Dependencias (DI)
Spring inyecta automáticamente las dependencias que un objeto necesita.

### Anotaciones esenciales

| Anotación | Descripción |
|-----------|-------------|
| `@SpringBootApplication` | Clase principal, activa toda la configuración |
| `@Component` | Marca una clase como componente de Spring |
| `@Service` | Componente de la capa de lógica de negocio |
| `@Repository` | Componente de la capa de acceso a datos |
| `@Autowired` | Inyecta una dependencia automáticamente |

---

# Arquitectura en Capas

Separar el proyecto en capas permite mantener el código organizado, mantenible y escalable.

| Capa | Responsabilidad |
|------|----------------|
| **Controller** | Recibe la petición HTTP y retorna la respuesta |
| **Service** | Aplica la lógica de negocio |
| **Repository** | Accede y persiste datos en la base de datos |
| **Model** | Representa la entidad / tabla de la base de datos |

### Flujo de una petición

```
Cliente HTTP → Controller → Service → Repository → Base de Datos
```

Cada capa tiene una responsabilidad única y solo se comunica con la capa adyacente.

---

# ¿Qué es una API REST?

**REST** (Representational State Transfer) es un estilo de arquitectura para diseñar servicios web basado en HTTP.

### Principios clave

<v-clicks>

- 🔗 **Recursos identificables** — cada entidad tiene su propia URL `/api/v1/cursos/1`
- 🚫 **Sin estado (stateless)** — cada petición contiene toda la información necesaria
- 📦 **Formato estándar** — las respuestas se devuelven en JSON
- 🏷️ **Versionar la API** — `/api/v1/` para no romper clientes con cambios futuros

</v-clicks>

---

# Verbos HTTP

| Verbo | Acción | ¿Modifica datos? |
|-------|--------|-----------------|
| `GET` | Obtener datos | ❌ No |
| `POST` | Crear un recurso | ✅ Sí |
| `PUT` | Actualizar recurso completo | ✅ Sí |
| `PATCH` | Actualizar recurso parcialmente | ✅ Sí |
| `DELETE` | Eliminar un recurso | ✅ Sí |

> El verbo define **qué** se hace · La URL define **sobre qué** se hace

---

# PUT vs PATCH

### PUT — Reemplaza el recurso completo
Debes enviar **todos los campos**. Si omites alguno, ese campo se pierde en la base de datos.

```
PUT /api/v1/cursos/1
→ Enviar: nombre, descripcion, precio, activo
```

### PATCH — Actualiza solo lo que cambia
Solo envías los campos que quieres modificar. El resto se mantiene intacto.

```
PATCH /api/v1/cursos/1
→ Enviar solo: precio
```

---

# Estándares de Diseño REST

| Regla | Correcto | Incorrecto |
|-------|----------|------------|
| Minúsculas | `/api/cursos` | `/api/Cursos` |
| Sustantivos | `/api/cursos` | `/api/obtenerCursos` |
| Plural | `/api/cursos` | `/api/curso` |
| Versión | `/api/v1/cursos` | `/api/cursos` |
| Sin verbos en URL | `DELETE /api/cursos/1` | `GET /api/eliminarCurso/1` |
| Query params para filtros | `?activo=true&page=1` | `/activo/true/pagina/1` |

---

# Códigos de Respuesta — 2xx Éxito

El servidor siempre responde con un código numérico que indica el resultado.

| Código | Nombre | Cuándo se usa |
|--------|--------|---------------|
| `200` | OK | GET, PUT, PATCH exitosos |
| `201` | Created | POST exitoso, recurso creado |
| `204` | No Content | DELETE exitoso, sin cuerpo en respuesta |

---

# Códigos de Respuesta — 4xx Error del Cliente

| Código | Nombre | Descripción |
|--------|--------|-------------|
| `400` | Bad Request | Datos inválidos o mal formados |
| `401` | Unauthorized | No autenticado, requiere login |
| `403` | Forbidden | Autenticado pero sin permisos |
| `404` | Not Found | El recurso no existe |
| `409` | Conflict | Duplicado o conflicto de datos |
| `422` | Unprocessable Entity | Falla validación de negocio |

---

# Códigos de Respuesta — 5xx Error del Servidor

| Código | Nombre | Descripción |
|--------|--------|-------------|
| `500` | Internal Server Error | Error inesperado del servidor |
| `502` | Bad Gateway | Respuesta inválida de otro servidor |
| `503` | Service Unavailable | Servidor en mantenimiento |
| `504` | Gateway Timeout | Tiempo de espera agotado |

> **Regla general:** 2xx ✅ todo bien · 4xx ❌ error del cliente · 5xx 💥 error del servidor

---

# Configuración de la Base de Datos

### Archivo application.properties
Archivo central de configuración de Spring Boot donde se define la conexión a la base de datos.

### Parámetros principales

| Parámetro | Descripción |
|-----------|-------------|
| `datasource.url` | URL de conexión a la base de datos |
| `datasource.username` | Usuario de la base de datos |
| `datasource.password` | Contraseña |
| `jpa.hibernate.ddl-auto` | Comportamiento del esquema al iniciar |
| `jpa.show-sql` | Muestra las consultas SQL en consola |

---

# ddl-auto y Opciones de Base de Datos

### ddl-auto — comportamiento al iniciar

| Valor | Comportamiento | Uso recomendado |
|-------|----------------|-----------------|
| `create` | Crea las tablas (borra datos anteriores) | Desarrollo inicial |
| `update` | Actualiza sin borrar datos | Desarrollo activo |
| `validate` | Solo valida, no modifica nada | QA / Staging |
| `none` | No hace nada | Producción |

### Opciones de base de datos

| BD | Característica |
|----|----------------|
| **H2** | En memoria, ideal para desarrollo y pruebas rápidas |
| **MySQL** | Relacional, muy usada en producción |
| **PostgreSQL** | Relacional avanzada, robusta y open source |

---

# ¿Qué es JPA e Hibernate?

### JPA (Java Persistence API)
Especificación estándar de Java que define cómo mapear objetos Java a tablas de base de datos. Es una interfaz, no una implementación.

### Hibernate
La implementación más popular de JPA. Spring Boot lo usa por defecto. Se encarga de traducir operaciones Java a SQL.

### Relación

| Capa | Rol |
|------|-----|
| Tu clase Java | Define la estructura del objeto |
| JPA | Especificación / contrato |
| Hibernate | Implementación que genera el SQL |
| Base de Datos | Almacena los datos |

---

# Entidad y Anotaciones JPA

### ¿Qué es una entidad?
Una clase Java que representa una tabla en la base de datos. Cada instancia de la clase es un registro en la tabla.

### Anotaciones de mapeo

| Anotación | Descripción |
|-----------|-------------|
| `@Entity` | Marca la clase como tabla en la BD |
| `@Table` | Especifica el nombre de la tabla |
| `@Id` | Define la clave primaria |
| `@GeneratedValue` | Configura el auto incremento del ID |
| `@Column` | Configura propiedades de una columna |

---

# Lombok

Biblioteca que genera automáticamente código repetitivo en tiempo de compilación.

| Anotación | Genera |
|-----------|--------|
| `@Data` | Getters, Setters, equals, hashCode, toString |
| `@NoArgsConstructor` | Constructor sin argumentos |
| `@AllArgsConstructor` | Constructor con todos los argumentos |
| `@Builder` | Patrón Builder para crear objetos |

### Beneficio
Sin Lombok una entidad simple puede superar las 50 líneas de código. Con Lombok se reduce únicamente a la declaración de atributos y anotaciones.

---

# Capa Repository

### ¿Qué es un Repository?
Interfaz que abstrae el acceso a la base de datos. Spring Data JPA genera la implementación automáticamente en tiempo de ejecución.

### Métodos heredados de JpaRepository

| Método | Descripción |
|--------|-------------|
| `findAll()` | Lista todos los registros |
| `findById(id)` | Busca por clave primaria |
| `save(entity)` | Crea o actualiza un registro |
| `deleteById(id)` | Elimina por clave primaria |
| `count()` | Cuenta el total de registros |
| `existsById(id)` | Verifica si un registro existe |

---

# Consultas Personalizadas en Repository

### Métodos por convención de nombres
Spring Data JPA interpreta el nombre del método y genera el SQL automáticamente.

| Método | SQL generado |
|--------|-------------|
| `findByNombre(String nombre)` | `WHERE nombre = ?` |
| `findByActivo(Boolean activo)` | `WHERE activo = ?` |
| `findByPrecioLessThan(Double precio)` | `WHERE precio < ?` |
| `findByNombreContaining(String texto)` | `WHERE nombre LIKE %?%` |

### @Query con JPQL
Para consultas más complejas se usa la anotación `@Query` con JPQL (Java Persistence Query Language), similar a SQL pero orientado a objetos en lugar de tablas.

---

# Capa Service

### ¿Por qué una capa Service?

<v-clicks>

- Separa la lógica de negocio del Controller
- Permite reutilizar lógica desde distintos puntos
- Facilita las pruebas unitarias
- El Controller solo recibe y responde, el Service decide qué hacer

</v-clicks>

### Patrón interfaz + implementación

| Clase | Responsabilidad |
|-------|----------------|
| `CursoService` (interfaz) | Define el contrato de operaciones disponibles |
| `CursoServiceImpl` (clase) | Implementa la lógica de cada operación |

---

# Excepción Personalizada

### ¿Por qué crear excepciones propias?
- Identifica claramente el tipo de error ocurrido
- Permite capturarla de forma específica
- Retorna el código HTTP correcto (`404 Not Found`)
- Mejora los mensajes de error para el cliente

### Flujo de una excepción

```
Repository no encuentra el registro
          ↓
Service lanza RecursoNoEncontradoException
          ↓
GlobalExceptionHandler la captura
          ↓
Retorna 404 con mensaje descriptivo en JSON
```

---

# Capa Controller

### Responsabilidad del Controller
- Recibir la petición HTTP
- Delegar el trabajo al Service
- Retornar la respuesta con el código HTTP correcto

### Anotaciones REST

| Anotación | Descripción |
|-----------|-------------|
| `@RestController` | Controlador REST, respuestas en JSON |
| `@RequestMapping` | Define la ruta base del controlador |
| `@PathVariable` | Extrae el valor de la URL `/cursos/{id}` |
| `@RequestBody` | Extrae el cuerpo JSON de la petición |
| `ResponseEntity` | Permite controlar el código HTTP de la respuesta |

---

# Endpoints del CRUD

| Método | URL | Descripción | Código |
|--------|-----|-------------|--------|
| `GET` | `/api/v1/cursos` | Listar todos los cursos | 200 |
| `GET` | `/api/v1/cursos/{id}` | Buscar curso por ID | 200 / 404 |
| `POST` | `/api/v1/cursos` | Crear nuevo curso | 201 |
| `PUT` | `/api/v1/cursos/{id}` | Actualizar curso completo | 200 |
| `PATCH` | `/api/v1/cursos/{id}` | Actualizar curso parcialmente | 200 |
| `DELETE` | `/api/v1/cursos/{id}` | Eliminar curso | 204 |

---

# Postman

### ¿Qué es Postman?
Herramienta para probar, documentar y gestionar APIs. Permite enviar peticiones HTTP y verificar las respuestas sin necesidad de un frontend.

### Conceptos clave

| Concepto | Descripción |
|----------|-------------|
| **Colección** | Grupo de requests organizados por proyecto |
| **Request** | Petición HTTP configurada con método, URL y body |
| **Environment** | Variables reutilizables como `{{base_url}}` |
| **Response** | Respuesta del servidor con código HTTP y JSON |

---

# Flujo de Prueba en Postman

Para cada endpoint del CRUD se verifica:

<v-clicks>

1. ✅ **Código HTTP correcto** — 200, 201, 204, 404 según el caso
2. ✅ **Cuerpo de respuesta** — JSON con la estructura esperada
3. ✅ **Caso exitoso** — datos válidos, recurso existente
4. ✅ **Caso de error** — ID inexistente retorna 404
5. ✅ **Validaciones** — datos inválidos retornan 400

</v-clicks>

---

# Validaciones

### ¿Por qué validar?
Evitar que datos incorrectos lleguen a la base de datos y retornar mensajes claros al cliente.

### Anotaciones de validación

| Anotación | Descripción |
|-----------|-------------|
| `@NotNull` | El campo no puede ser nulo |
| `@NotBlank` | No puede ser nulo ni cadena vacía |
| `@Size` | Define longitud mínima y máxima del texto |
| `@Min` / `@Max` | Valor mínimo y máximo para números |
| `@Email` | Debe tener formato de correo electrónico |
| `@Valid` | Activa las validaciones en el Controller |

---

# Manejo Global de Excepciones

### @RestControllerAdvice
Clase centralizada que captura excepciones lanzadas desde cualquier Controller y retorna una respuesta JSON estandarizada.

### Excepciones más comunes

| Excepción | Código HTTP | Causa |
|-----------|-------------|-------|
| `RecursoNoEncontradoException` | 404 | Recurso no existe en BD |
| `MethodArgumentNotValidException` | 400 | Falla de validación en el body |
| `Exception` | 500 | Error inesperado del servidor |

### Estructura de respuesta de error

```
{ "status": 404, "error": "Not Found", "mensaje": "Curso no encontrado con id: 99" }
```

---

---
layout: center
class: text-center
---

# ¡A construir el CRUD!

<div class="text-gray-400 mt-4">
Spring Boot · JPA · Hibernate · REST · Postman
</div>

<div class="pt-8 text-sm text-gray-500">
Controller → Service → Repository → Base de Datos
</div>
