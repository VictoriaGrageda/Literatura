# 📚 Literalura

Literalura es una aplicación de consola desarrollada en **Java 21** con **Spring Boot** y **Maven**, orientada a la búsqueda, almacenamiento y consulta de libros y autores a partir de la API pública [Gutendex](https://gutendex.com/). La información obtenida se guarda en una base de datos **PostgreSQL**, lo que permite trabajar con registros persistentes y realizar consultas posteriores.

## 👤 Autor

**Victoria Grageda**

---

## 🛠️ Tecnologías utilizadas

- Java 21
- Spring Boot
- Maven
- Spring Data JPA / Hibernate
- PostgreSQL
- Jackson Databind para deserialización de datos JSON
- API Gutendex (`https://gutendex.com`)

---

## 📋 Funcionalidades

La aplicación permite consultar información literaria desde la API y gestionar los datos almacenados en la base de datos local.

| Opción | Descripción |
|--------|-------------|
| 1 | Buscar un libro en la API y agregarlo a la base de datos |
| 2 | Buscar un libro registrado por título |
| 3 | Mostrar todos los libros almacenados |
| 4 | Mostrar todos los autores registrados |
| 5 | Consultar autores vivos en un año determinado |
| 6 | Listar libros según el idioma |
| 7 | Mostrar el Top 10 de libros más descargados |
| 0 | Salir de la aplicación |

---

## ⚙️ Configuración

### 1. Requisitos previos

Antes de ejecutar el proyecto, asegúrate de contar con lo siguiente:

- Java 21 instalado
- PostgreSQL instalado y en ejecución
- Una base de datos creada con el nombre `literalura`

### 2. Variables de entorno

Para proteger las credenciales de acceso a la base de datos, la aplicación utiliza variables de entorno.

| Variable | Descripción |
|----------|-------------|
| `DB_HOST` | Host de la base de datos, por ejemplo: `localhost` |
| `DB_USER` | Usuario de PostgreSQL |
| `DB_PASSWORD` | Contraseña de PostgreSQL |

---

## ▶️ Cómo ejecutar el proyecto

1. Clona el repositorio o descarga el proyecto.
2. Configura las variables de entorno con tus credenciales de PostgreSQL.
3. Verifica que la base de datos `literalura` exista.
4. Ejecuta la aplicación desde tu IDE o mediante Maven.
5. Usa el menú en consola para interactuar con las opciones disponibles.

---

## 📌 Consideraciones

- Si un autor ya existe en la base de datos, el sistema reutiliza su registro para evitar duplicados.
- Si un libro ya fue almacenado previamente, la aplicación informa al usuario y evita registrarlo nuevamente.
- Algunos libros pueden guardarse con idioma `null` si la información recibida no coincide con los idiomas definidos en el sistema.
- La búsqueda por título no distingue entre mayúsculas y minúsculas.

---

## 🌐 API utilizada

La información de libros y autores se obtiene desde la API pública de [Gutendex](https://gutendex.com/), la cual ofrece acceso a obras literarias de dominio público.

---

## 📎 Repositorio

Puedes acceder al repositorio del proyecto en el siguiente enlace:

[Literalura - Repositorio en GitHub](https://github.com/VictoriaGrageda/Literatura.git)

---

Proyecto desarrollado como parte del **Challenge de Spring Boot de Alura Latam**, con adaptaciones personales en la organización y presentación del sistema.