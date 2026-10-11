# Temario: CRUD con Spring Boot y Persistencia con JPA/Hibernate

> **Nivel:** Intermedio (requiere conocimientos en Java)
> **Objetivo:** Construir un CRUD completo con Spring Boot, JPA/Hibernate y base de datos relacional, probando los endpoints con Postman.

---

## Módulo 1 — Introducción y Configuración del Entorno

1.1 ¿Qué es Spring Boot y por qué usarlo?
1.2 Requisitos previos
   - JDK 21 instalado
   - Maven configurado
   - IDE (IntelliJ IDEA / VS Code)
   - Postman instalado

1.3 Crear un proyecto con Spring Initializr
   - Selección de dependencias: Spring Web, Spring Data JPA, Driver de BD
   - Estructura del proyecto generado
   - Archivos clave: `pom.xml`, `application.properties`

1.4 Ejecutar el proyecto por primera vez

---

## Módulo 2 — Conceptos Clave de Spring Boot

2.1 Inversión de Control (IoC) e Inyección de Dependencias (DI)
2.2 Anotaciones esenciales
   - `@SpringBootApplication`
   - `@Component`, `@Service`, `@Repository`
   - `@Autowired`
2.3 Arquitectura en capas
   - Controller → Service → Repository → Base de Datos
2.4 ¿Qué es Spring Data JPA?
2.5 ¿Qué es Hibernate y cómo se relaciona con JPA?

---

## Módulo 3 — Configuración de la Base de Datos

3.1 Configurar la conexión en `application.properties`
   - URL, usuario, contraseña
   - Dialecto de Hibernate
   - `spring.jpa.hibernate.ddl-auto`

3.2 Opciones de base de datos
   - H2 (en memoria, para desarrollo rápido)
   - MySQL
   - PostgreSQL

3.3 Verificar la conexión al arrancar la aplicación

---

## Módulo 4 — Creando la Entidad

4.1 ¿Qué es una entidad JPA?
4.2 Anotaciones de mapeo
   - `@Entity`, `@Table`
   - `@Id`, `@GeneratedValue`
   - `@Column`
4.3 Crear la entidad `Curso`
   - id, nombre, descripcion, precio, activo
4.4 Estrategias de generación de ID
   - `IDENTITY`, `SEQUENCE`, `AUTO`
4.5 Lombok para reducir código boilerplate
   - `@Data`, `@NoArgsConstructor`, `@AllArgsConstructor`, `@Builder`

---

## Módulo 5 — Capa Repository

5.1 ¿Qué es un Repository en Spring Data JPA?
5.2 Extender `JpaRepository`
   - Métodos heredados: `findAll`, `findById`, `save`, `deleteById`
5.3 Consultas personalizadas
   - Métodos por convención: `findByNombre`, `findByActivo`
   - `@Query` con JPQL
5.4 Diferencia entre `CrudRepository`, `JpaRepository` y `PagingAndSortingRepository`

---

## Módulo 6 — Capa Service

6.1 ¿Por qué separar la lógica en un Service?
6.2 Crear la interfaz `CursoService`
6.3 Implementar `CursoServiceImpl`
   - Listar todos los cursos
   - Buscar por ID
   - Crear curso
   - Actualizar curso
   - Eliminar curso
6.4 Manejo de excepciones
   - Crear excepción personalizada `RecursoNoEncontradoException`
   - Lanzar excepción cuando el recurso no existe

---

## Módulo 7 — Capa Controller (API REST)

7.1 Anotaciones REST
   - `@RestController`, `@RequestMapping`
   - `@GetMapping`, `@PostMapping`, `@PutMapping`, `@PatchMapping`, `@DeleteMapping`
7.2 Crear `CursoController` con los 5 endpoints del CRUD
7.3 `@PathVariable` y `@RequestBody`
7.4 Usar `ResponseEntity` para controlar códigos HTTP
   - `200 OK`, `201 Created`, `204 No Content`, `404 Not Found`
7.5 Estándares REST en las URLs
   - Versionar la API: `/api/v1/cursos`

---

## Módulo 8 — Probando el CRUD con Postman

8.1 Introducción a Postman
   - Instalación y configuración
   - Crear una colección

8.2 Probar cada endpoint
   - `GET /api/v1/cursos` — listar todos
   - `GET /api/v1/cursos/{id}` — buscar por ID
   - `POST /api/v1/cursos` — crear curso (body en JSON)
   - `PUT /api/v1/cursos/{id}` — actualizar curso completo
   - `PATCH /api/v1/cursos/{id}` — actualizar parcialmente
   - `DELETE /api/v1/cursos/{id}` — eliminar curso

8.3 Verificar códigos de respuesta HTTP
8.4 Exportar la colección de Postman

---

## Módulo 9 — Validaciones

9.1 Agregar dependencia `spring-boot-starter-validation`
9.2 Anotaciones de validación en la entidad
   - `@NotNull`, `@NotBlank`, `@Size`, `@Min`, `@Max`
9.3 Activar validaciones con `@Valid` en el Controller
9.4 Manejar errores de validación con `@ExceptionHandler`
9.5 Respuesta de error estandarizada en JSON

---

## Módulo 10 — Manejo Global de Excepciones

10.1 `@ControllerAdvice` y `@ExceptionHandler`
10.2 Crear clase `GlobalExceptionHandler`
10.3 Manejar excepciones comunes
   - `RecursoNoEncontradoException` → 404
   - `MethodArgumentNotValidException` → 400
   - `Exception` genérica → 500
10.4 Estructura de respuesta de error consistente

---

## Módulo 11 — Pruebas Unitarias y Diagramas UML

11.1 Pruebas unitarias con JUnit 5 y Mockito
   - Dependencias: `spring-boot-starter-test`
   - Estructura de una prueba unitaria
   - Anotaciones: `@Test`, `@BeforeEach`, `@AfterEach`

11.2 Pruebas del Service con Mockito
   - `@Mock` y `@InjectMocks`
   - Simular comportamiento del Repository con `when().thenReturn()`
   - Verificar llamadas con `verify()`

11.3 Pruebas del Controller con MockMvc
   - `@WebMvcTest`
   - Simular peticiones HTTP
   - Verificar respuestas y códigos HTTP

11.4 Diagramas UML del proyecto
   - Diagrama de clases: entidades y relaciones
   - Diagrama de secuencia: flujo de una petición REST
   - Diagrama de componentes: arquitectura en capas
   - Herramientas: PlantUML, draw.io, StarUML

---

## Módulo 12 — Calidad de Código

12.1 Principios SOLID
   - S — Responsabilidad única
   - O — Abierto/Cerrado
   - L — Sustitución de Liskov
   - I — Segregación de interfaces
   - D — Inversión de dependencias

12.2 DTOs y mappers
   - ¿Por qué no exponer las entidades directamente?
   - Patrón DTO (Data Transfer Object)
   - MapStruct para mapeo automático

12.3 Clean Code
   - Nombres descriptivos
   - Métodos cortos y con una sola responsabilidad
   - Evitar código duplicado (DRY)
   - Code smells comunes

12.4 Métricas y análisis estático
   - Cobertura de pruebas con JaCoCo
   - Análisis estático con SonarQube
   - Deuda técnica

---

## Módulo 13 — Proyecto Final

11.1 Construir el CRUD completo de la entidad `Curso` aplicando todos los módulos
11.2 Verificar todos los endpoints con Postman
11.3 Revisar buenas prácticas aplicadas
   - Separación de capas
   - Manejo de excepciones
   - Validaciones
   - Estándares REST
11.4 Exportar y documentar la colección de Postman

---

## Herramientas utilizadas en el curso

| Herramienta | Versión | Uso |
|-------------|---------|-----|
| Java | 21 | Lenguaje principal |
| Spring Boot | 3.2.x | Framework |
| Maven | 3.9.x | Gestión de dependencias |
| Spring Data JPA | - | Persistencia |
| Hibernate | - | ORM |
| H2 / MySQL / PostgreSQL | - | Base de datos |
| Lombok | - | Reducir boilerplate |
| Postman | Latest | Pruebas de endpoints |
| IntelliJ IDEA / VS Code | - | IDE |

---

> **Resultado esperado:** Al finalizar el curso tendrás un CRUD funcional con Spring Boot, persistencia con JPA/Hibernate, validaciones, manejo de excepciones y todos los endpoints probados con Postman.
