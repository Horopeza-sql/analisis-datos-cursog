# 02 · Fundamentos de Base de Datos y Creación de Tablas

## 🎯 Objetivo de Aprendizaje
Aprender a definir estructuras en una base de datos relacional utilizando sentencias DDL (`CREATE DATABASE`, `USE`, `CREATE TABLE`) y entender los tipos de datos fundamentales.

---

## 💡 El Problema de Negocio

Para registrar las ventas y cobranzas de la empresa de manera ordenada, necesitamos un lugar donde almacenar la información evitando datos duplicados y asegurando que cada registro tenga un identificador único.

---

## 🔑 Conceptos Clave de Modelado

- **Base de Datos (Schema):** Es el contenedor global que agrupa todas las tablas relacionadas de un sistema.
- **Tabla:** Estructura bidimensional de filas (registros) y columnas (atributos).
- **Llave Primaria (Primary Key):** Campo único e irrepetible que identifica cada fila de una tabla (ej. `id_cliente`).
- **Tipos de Datos Principales:**
  - `INT`: Números enteros (ej. IDs, cantidades).
  - `VARCHAR(N)`: Texto de longitud variable de hasta $N$ caracteres (ej. nombres, direcciones).
  - `DECIMAL(M, D)`: Números precisos con decimales, ideal para importes financieros (ej. salarios, límites de crédito).
  - `DATE`: Fechas en formato `YYYY-MM-DD`.

---

## 📝 Sentencias DDL del Módulo

```sql
CREATE DATABASE IF NOT EXISTS sistema_ventas;
USE sistema_ventas;

CREATE TABLE IF NOT EXISTS clientes (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nombre_empresa VARCHAR(100) NOT NULL,
    rif_identificacion VARCHAR(20) UNIQUE NOT NULL,
    ciudad VARCHAR(50),
    limite_credito DECIMAL(12, 2) DEFAULT 0.00,
    fecha_registro DATE DEFAULT CURRENT_DATE
);

CREATE TABLE IF NOT EXISTS productos (
    id_producto INT AUTO_INCREMENT PRIMARY KEY,
    nombre_producto VARCHAR(100) NOT NULL,
    categoria VARCHAR(50),
    precio_unitario DECIMAL(10, 2) NOT NULL
);