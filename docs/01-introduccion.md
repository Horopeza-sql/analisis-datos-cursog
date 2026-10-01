# 01 · Introducción a SQL y el Entorno de Trabajo

## 🎯 Objetivo de Aprendizaje
Al finalizar este módulo, entenderás qué es una base de datos relacional, qué rol cumple SQL en el análisis de datos y tendrás listo tu entorno de trabajo con MySQL y MySQL Workbench.

---

## 💡 El Problema de Negocio

En cualquier empresa, la información de ventas, inventario y cuentas por cobrar suele empezar en hojas de cálculo de Excel. Sin embargo, a medida que la empresa crece, Excel se vuelve lento, repetitivo y propenso a errores.

Para analizar millones de registros de forma rápida, segura y centralizada, las empresas organizan su información en **Bases de Datos Relacionales**.

---

## 🤔 ¿Qué es SQL y por qué lo necesita un Analista?

**SQL** (*Structured Query Language* o Lenguaje de Consulta Estructurado) es el estándar universal para comunicarte con una base de datos.

Como analista, no utilizas SQL para programar aplicaciones, sino para **hacerle preguntas a los datos**:

- ¿Cuánto vendimos este mes por región?
- ¿Cuáles clientes tienen facturas vencidas a más de 30 días?
- ¿Cuál es el ticket promedio de compra por producto?

---

## ⚙️ Las Herramientas del Entorno

Para trabajar con SQL necesitaremos dos componentes principales:

1. **MySQL Server (El Motor):** Es el programa que almacena, procesa y resguarda los datos en la computadora o servidor.
2. **MySQL Workbench (La Interfaz Visual):** Es la ventana gráfica donde escribiremos nuestras consultas SQL, veremos los resultados en tablas y gestionaremos las conexiones.

---

## 🖥️ Preparación e Instalación

Para instalar ambas herramientas en tu computadora:

1. Descarga el instalador oficial de **MySQL Installer for Windows** desde la página de MySQL.
2. Selecciona la opción **Developer Default** o instala directamente **MySQL Server 8.4 LTS** y **MySQL Workbench**.
3. Durante la configuración, asigna una contraseña sencilla para el usuario administrador (`root`) y guárdala en un lugar seguro.

> 💡 **Nota alternativa:** Si prefieres no instalar programas locales al inicio, puedes practicar los comandos en herramientas web en línea como [DB-Fiddle](https://www.db-fiddle.com/) o [SQL Fiddle](https://sqlfiddle.com/).

---

## 🎯 Práctica del Módulo

🟢 **Nivel 1 — Guiado (Verificación de entorno)**

1. Abre **MySQL Workbench** en tu computadora.
2. Haz clic en la conexión local (**Local instance MySQL80** e ingresa la contraseña de tu usuario `root`).
3. En el editor de texto que aparece, escribe la siguiente consulta de prueba:

```sql
SELECT '¡Entorno configurado con éxito!' AS mensaje;