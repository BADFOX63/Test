# Proyecto Java JDBC - Módulo CRUD de Usuario

## Descripción

Este proyecto es un ejemplo básico de un módulo de software en Java que realiza operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre una entidad `Usuario` utilizando JDBC para conectarse a una base de datos MySQL.

---

## Estructura del proyecto

src/
└── main/
└── java/
└── com/
└── tuempresa/
└── proyecto/
├── app/
│ └── MainApp.java
├── dao/
│ ├── ConexionDB.java
│ └── UsuarioDAO.java
└── modelo/
└── Usuario.java


---

## Requisitos

- Java JDK 8 o superior
- MySQL Server
- IDE para Java (Eclipse, IntelliJ, NetBeans, etc.)
- Driver JDBC para MySQL (por ejemplo, `mysql-connector-java`)

---

## Configuración

1. Crear la base de datos y la tabla en MySQL:

```sql
CREATE DATABASE nombreBaseDatos;

USE nombreBaseDatos;

CREATE TABLE usuarios (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nombre VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL
);

Modificar la clase ConexionDB.java con los datos de conexión correctos (URL, usuario, contraseña):

private static final String URL = "jdbc:mysql://localhost:3306/nombreBaseDatos";
private static final String USUARIO = "admin";
private static final String PASSWORD = "admin123";