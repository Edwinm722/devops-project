# Infraestructura DevOps en la Nube

Proyecto Final — Sistemas Operativos II
Universidad Mariano Galvez de Guatemala
Estudiante: Edwin Mendez Castro | Carnet: 0910-23-6496

## Descripcion

Infraestructura moderna basada en practicas DevOps desplegada en AWS con contenedores Docker, orquestacion con Docker Swarm y pipeline CI/CD automatizado con GitHub Actions.

## Tecnologias

- Cloud: Amazon Web Services (EC2, VPC, Security Groups)
- Contenedores: Docker 29.1.3 + Docker Compose
- Orquestacion: Docker Swarm
- CI/CD: GitHub Actions
- App: Nginx alpine
- Base de datos: MySQL 8.0
- OS: Ubuntu 26.04 LTS

## Arquitectura

- EC2 t3.micro en us-east-2 Ohio
- IP publica: 3.14.15.220
- 2 replicas del servicio web
- 1 replica de MySQL
- Red overlay interna entre servicios

## Acceso

- http://3.14.15.220
- http://3.14.15.220:8080

## Pipeline CI/CD

Cada push a main dispara automaticamente:
1. Checkout del repositorio
2. Build de imagen Docker
3. Pruebas basicas
4. Deploy automatico al servidor via SSH
