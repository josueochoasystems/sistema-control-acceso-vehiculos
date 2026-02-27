# 🚗 Sistema de Control de Acceso Vehicular IoT con RFID

Sistema de control de acceso vehicular basado en tecnología **IoT**, que integra hardware y software para gestionar entradas y salidas de vehículos mediante identificación por **RFID**.

El proyecto combina **Spring Boot**, **MySQL**, **Arduino UNO** y un **módulo RFID**, permitiendo una solución completa de seguridad y automatización.

---

## 📌 Descripción del Proyecto

Este sistema implementa una solución tecnológica para el **control de acceso vehicular**, donde cada vehículo es identificado a través de una tarjeta RFID.

El Arduino se encarga de la lectura de tarjetas, mientras que el backend en Spring Boot procesa la información, valida accesos y almacena los registros en MySQL.

El objetivo del proyecto es demostrar la integración de tecnologías **IoT + Backend Empresarial**.

---

## 🧰 Tecnologías Utilizadas

### 🔹 Backend
- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **Maven**
- **Swagger / OpenAPI**

### 🔹 Base de Datos
- **MySQL**

### 🔹 Hardware / IoT
- **Arduino UNO**
- **Módulo RFID (RC522 / RFID32)**
- **Comunicación Serial / HTTP**

---

## 🏗️ Arquitectura del Sistema

El sistema está compuesto por los siguientes módulos:

✔ **Dispositivo IoT (Arduino + RFID)**  
✔ **API REST (Spring Boot)**  
✔ **Base de Datos (MySQL)**  
✔ **Documentación API (Swagger UI)**  

### Flujo de operación

Tarjeta RFID → Arduino → Backend → Base de Datos


---

## ⚙️ Funcionalidades Principales

✅ Registro de vehículos  
✅ Validación de tarjetas RFID  
✅ Control de entradas / salidas  
✅ Persistencia de datos en MySQL  
✅ Exposición de API REST  
✅ Documentación automática con Swagger  

---

## 🗄️ Modelo de Datos

El sistema maneja entidades como:

- Vehículo
- Tarjeta RFID
- Registro de Acceso

### Ejemplo de información procesada

```json
{
  "uid": "A1B2C3D4",
  "evento": "ENTRADA",
  "fecha": "2026-02-16T19:00:00"
}

```

🚀 Ejecución del Proyecto

✅ 1️⃣ Requisitos Previos
Instalar:

Java 17+

Maven

MySQL

Arduino IDE

Git


✅ 2️⃣ Configuración Base de Datos
CREATE DATABASE registro_carros;


✅ 3️⃣ Configuración Backend

Editar:

src/main/resources/application.properties

spring.datasource.url=jdbc:mysql://localhost:3306/registro_carros

spring.datasource.username=root

spring.datasource.password=TU_PASSWORD

spring.jpa.hibernate.ddl-auto=update


✅ 4️⃣ Ejecutar Backend
Desde terminal:

mvn spring-boot:run

O desde IDE:

Run → Spring Boot App

📖 Documentación API

Swagger UI disponible en:

http://localhost:8082/doc/swagger-ui.html

🔌 Integración IoT


El Arduino:

✔ Lee tarjetas RFID

✔ Envía datos al backend

✔ Permite automatizar acciones físicas (barrera, LEDs, etc.)

Comunicación típica

Arduino → API REST → Registro en BD


📈 Posibles Mejoras Futuras

✅ Panel administrativo web

✅ Autenticación y roles

✅ Historial avanzado de accesos

✅ Reportes y estadísticas

✅ Integración con sensores adicionales


---

## 👨‍💻 Autor

**Josue Ochoa**  
Estudiante de Ingeniería de Sistemas

---

✨ *Gracias por visitar el proyecto* ✨