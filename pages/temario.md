---
layout: section
background: https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1920&q=40
---

<div class="text-white text-sm tracking-widest uppercase font-semibold mb-2">Temario del Curso</div>

# CRUD con Spring Boot y JPA

<div class="text-gray-200 mt-2">Nivel Intermedio · 13 Módulos</div>

---
transition: slide-up
---

# Temario — Módulos 1 al 4

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 rounded-xl border border-blue-200 bg-blue-50 shadow-sm">
  <div class="text-blue-600 font-bold mb-2">📦 Módulo 1 — Introducción</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>¿Qué es Spring Boot y por qué usarlo?</li>
    <li>Requisitos previos (JDK 21, Maven, IDE)</li>
    <li>Crear proyecto con Spring Initializr</li>
    <li>Ejecutar el proyecto por primera vez</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-green-200 bg-green-50 shadow-sm">
  <div class="text-green-600 font-bold mb-2">⚙️ Módulo 2 — Conceptos Clave</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>IoC e Inyección de Dependencias</li>
    <li>Anotaciones: @Component, @Service, @Repository</li>
    <li>Arquitectura en capas</li>
    <li>JPA, Hibernate y su relación</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-yellow-200 bg-yellow-50 shadow-sm">
  <div class="text-yellow-600 font-bold mb-2">🗄️ Módulo 3 — Base de Datos</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>Configurar application.properties</li>
    <li>URL, usuario, contraseña, ddl-auto</li>
    <li>H2 · MySQL · PostgreSQL</li>
    <li>Verificar la conexión al arrancar</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-purple-200 bg-purple-50 shadow-sm">
  <div class="text-purple-600 font-bold mb-2">📋 Módulo 4 — Entidad JPA</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>@Entity, @Table, @Id, @GeneratedValue</li>
    <li>Crear entidad Curso (id, nombre, precio…)</li>
    <li>Estrategias de generación de ID</li>
    <li>Lombok: @Data, @Builder, @NoArgsConstructor</li>
  </ul>
</div>

</div>

---
transition: slide-up
---

# Temario — Módulos 5 al 8

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 rounded-xl border border-green-200 bg-green-50 shadow-sm">
  <div class="text-green-600 font-bold mb-2">🗂️ Módulo 5 — Repository</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>Extender JpaRepository</li>
    <li>findAll, findById, save, deleteById</li>
    <li>Consultas por convención de nombres</li>
    <li>@Query con JPQL</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-blue-200 bg-blue-50 shadow-sm">
  <div class="text-blue-600 font-bold mb-2">⚙️ Módulo 6 — Service</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>Interfaz CursoService</li>
    <li>Implementar CursoServiceImpl</li>
    <li>Listar, buscar, crear, actualizar, eliminar</li>
    <li>Excepción RecursoNoEncontradoException</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-orange-200 bg-orange-50 shadow-sm">
  <div class="text-orange-600 font-bold mb-2">🌐 Módulo 7 — Controller REST</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>@RestController, @RequestMapping</li>
    <li>5 endpoints del CRUD</li>
    <li>@PathVariable, @RequestBody</li>
    <li>ResponseEntity — códigos HTTP</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-red-200 bg-red-50 shadow-sm">
  <div class="text-red-600 font-bold mb-2">🧪 Módulo 8 — Postman</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>Crear colección y requests</li>
    <li>Probar GET, POST, PUT, PATCH, DELETE</li>
    <li>Verificar códigos de respuesta</li>
    <li>Exportar la colección</li>
  </ul>
</div>

</div>

---
transition: slide-up
---

# Temario — Módulos 9 al 11

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="p-4 rounded-xl border border-indigo-200 bg-indigo-50 shadow-sm">
  <div class="text-indigo-600 font-bold mb-2 text-sm">✅ Módulo 9 — Validaciones</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>spring-boot-starter-validation</li>
    <li>@NotNull, @NotBlank, @Size</li>
    <li>@Valid en el Controller</li>
    <li>Respuesta de error en JSON</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-red-200 bg-red-50 shadow-sm">
  <div class="text-red-600 font-bold mb-2 text-sm">🛡️ Módulo 10 — Excepciones</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>@RestControllerAdvice</li>
    <li>GlobalExceptionHandler</li>
    <li>404 · 400 · 500</li>
    <li>Respuesta de error consistente</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-pink-200 bg-pink-50 shadow-sm">
  <div class="text-pink-600 font-bold mb-2 text-sm">🧪 Módulo 11 — Pruebas y UML</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>JUnit 5 y Mockito</li>
    <li>Pruebas con @Mock e @InjectMocks</li>
    <li>Controller con MockMvc</li>
    <li>Diagramas UML</li>
  </ul>
</div>

</div>

---
transition: slide-up
---

# Temario — Módulos 12 y 13

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 rounded-xl border border-cyan-200 bg-cyan-50 shadow-sm">
  <div class="text-cyan-600 font-bold mb-2">⭐ Módulo 12 — Calidad de Código</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>Principios SOLID</li>
    <li>DTOs y mappers (MapStruct)</li>
    <li>Clean Code y code smells</li>
    <li>JaCoCo y SonarQube</li>
  </ul>
</div>

<div class="p-4 rounded-xl border border-emerald-200 bg-emerald-50 shadow-sm">
  <div class="text-emerald-600 font-bold mb-2">🚀 Módulo 13 — Proyecto Final</div>
  <ul class="text-xs text-gray-600 space-y-1">
    <li>✅ CRUD completo de la entidad Curso</li>
    <li>✅ Endpoints verificados con Postman</li>
    <li>✅ Buenas prácticas aplicadas</li>
    <li>✅ Colección de Postman exportada</li>
  </ul>
</div>

</div>

---
transition: slide-up
---

# Herramientas del Curso

<div class="grid grid-cols-3 gap-3 mt-4">

<div class="p-3 rounded-xl border border-gray-200 bg-gray-50 text-center shadow-sm">
  <div class="flex justify-center mb-1"><logos-java class="text-3xl" /></div>
  <div class="text-gray-700 font-bold text-sm">Java 21</div>
  <div class="text-xs text-gray-400">Lenguaje principal</div>
</div>

<div class="p-3 rounded-xl border border-green-200 bg-green-50 text-center shadow-sm">
  <div class="flex justify-center mb-1"><logos-spring-icon class="text-3xl" /></div>
  <div class="text-green-700 font-bold text-sm">Spring Boot 3.2</div>
  <div class="text-xs text-gray-400">Framework</div>
</div>

<div class="p-3 rounded-xl border border-blue-200 bg-blue-50 text-center shadow-sm">
  <div class="flex justify-center mb-1"><logos-maven class="text-3xl" /></div>
  <div class="text-blue-700 font-bold text-sm">Maven 3.9</div>
  <div class="text-xs text-gray-400">Gestión de dependencias</div>
</div>

<div class="p-3 rounded-xl border border-purple-200 bg-purple-50 text-center shadow-sm">
  <div class="flex justify-center mb-1"><logos-hibernate class="text-3xl" /></div>
  <div class="text-purple-700 font-bold text-sm">Spring Data JPA</div>
  <div class="text-xs text-gray-400">Persistencia</div>
</div>

<div class="p-3 rounded-xl border border-orange-200 bg-orange-50 text-center shadow-sm">
  <div class="flex justify-center mb-1 gap-1"><logos-mysql-icon class="text-3xl" /><logos-postgresql class="text-3xl" /></div>
  <div class="text-orange-700 font-bold text-sm">H2 / MySQL / PostgreSQL</div>
  <div class="text-xs text-gray-400">Base de datos</div>
</div>

<div class="p-3 rounded-xl border border-red-200 bg-red-50 text-center shadow-sm">
  <div class="flex justify-center mb-1"><logos-postman-icon class="text-3xl" /></div>
  <div class="text-red-700 font-bold text-sm">Postman</div>
  <div class="text-xs text-gray-400">Pruebas de endpoints</div>
</div>

</div>

<div class="mt-4 p-3 rounded-xl border border-emerald-200 bg-emerald-50 text-center text-sm text-emerald-700 shadow-sm">
  🎯 <strong>Resultado:</strong> CRUD funcional con Spring Boot, JPA, validaciones, manejo de excepciones y endpoints probados con Postman.
</div>

<div class="mt-6 flex justify-center">
  <button @click="$slidev.nav.go(45)" class="px-6 py-2 rounded-full border border-blue-300 bg-blue-100 text-blue-700 text-sm font-medium hover:bg-blue-200 transition-colors cursor-pointer shadow-sm">
    📖 Ir al Contenido del Curso →
  </button>
</div>
