# 🏥 Spring PetClinic REST

[![Java](https://img.shields.io/badge/Java-21-red)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7-green)](https://spring.io/projects/spring-boot)
[![Maven](https://img.shields.io/badge/Maven-3.8.8-yellow)](https://maven.apache.org/)

## 📋 Descripción del Proyecto

Spring PetClinic REST es una API RESTful desarrollada con Spring Boot para la gestión administrativa de una clínica veterinaria. El proyecto implementa un pipeline completo de Integración Continua y Entrega Continua (CI/CD) utilizando Jenkins, SonarQube y JFrog Artifactory.

## 🎯 Funcionalidades

**Gestión de Veterinarios**
- Crear, leer, actualizar y eliminar veterinarios
- Listar todos los veterinarios
- Buscar veterinarios por especialidad

**Gestión de Dueños**
- Registro de dueños de mascotas
- Actualización de datos de contacto
- Historial de dueños

**Gestión de Mascotas**
- Registro de mascotas con sus datos
- Asignación de mascotas a dueños
- Control de tipos de mascotas (perro, gato, etc.)

**Gestión de Visitas**
- Registro de visitas veterinarias
- Historial de atención por mascota
- Control de fechas y diagnósticos

**API RESTful**
- Endpoints documentados con Swagger
- Respuestas en formato JSON
- Manejo de errores HTTP

## 🛠️ Tecnologías Utilizadas

- **Java 21**: Lenguaje de programación
- **Spring Boot 2.7**: Framework principal
- **Spring Data JPA**: Persistencia de datos
- **H2 Database**: Base de datos en memoria
- **Maven 3.8.8**: Gestión de dependencias
- **JUnit 5**: Pruebas unitarias
- **JaCoCo**: Cobertura de código
- **SonarQube**: Análisis de calidad de código
- **JFrog Artifactory**: Repositorio de artefactos
- **Jenkins**: Automatización CI/CD
- **Docker**: Contenedorización

## 📦 Instalación y Uso

## Requisitos Previos

- Java 21
- Maven 3.8.8
- Git

## Clonar el Repositorio

`git clone https://github.com/VicoVillca/spring-petclinic-rest.git`

`cd spring-petclinic-rest`

## Compilar el Proyecto

`mvn clean compile`

## Ejecutar Pruebas

`mvn test`

## Generar Reporte de Cobertura

`mvn jacoco:report`

## Generar el Artefacto

`mvn package -DskipTests`

## Ejecutar la Aplicación

`java -jar target/spring-petclinic-rest-*.jar`

## Acceder a la API

`http://localhost:9966/petclinic/api/`

## 📂 Estructura del Proyecto

spring-petclinic-rest/
├── src/
│ ├── main/
│ │ ├── java/ # Código fuente
│ │ └── resources/ # Configuraciones
│ └── test/
│ └── java/ # Pruebas unitarias
├── target/ # Artefactos generados
├── Jenkinsfile # Pipeline CI/CD
├── pom.xml # Dependencias
└── README.md # Documentación


## 👤 Autor

**VicoVillca**
- GitHub: [@VicoVillca](https://github.com/VicoVillca)

## 📄 Licencia

MIT License