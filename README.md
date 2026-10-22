# Sistema de Gestión de Pedidos - API REST

Este proyecto es una API REST desarrollada en **Spring Boot** y **MySQL** para la gestión de usuarios y pedidos comerciales. Fue creado como parte del plan de recuperación para demostrar la cultura **Docs as Code**.

## 🚀 Prerrequisitos
*   Java JDK 17 o superior.
*   Maven.
*   MySQL (se utilizó XAMPP en local).
*   Postman (para probar los endpoints).

## ⚙️ Variables de Entorno y Configuración
El archivo de configuración se encuentra en `src/main/resources/application.properties`.
Asegúrate de tener tu base de datos MySQL corriendo con el nombre `gestion_pedidos`.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/gestion_pedidos?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true
spring.datasource.username=root
spring.datasource.password=