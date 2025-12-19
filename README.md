#  Spring Data REST – Gestion des Comptes Bancaires

## 📌 Description
Ce TP est permettant de gérer des comptes bancaires (COURANT et EPARGNE) en utilisant **Spring Data REST**.  
L’objectif principal est d’exposer automatiquement des services RESTful à partir des repositories JPA, sans créer manuellement de contrôleurs REST.

L’application utilise une base de données **H2 en mémoire** et permet d’effectuer les opérations CRUD de base ainsi que des recherches personnalisées.

---

## 🛠️ Technologies utilisées
- Java 17+
- Spring Boot
- Spring Data JPA
- Spring Data REST
- H2 Database (In-Memory)
- Lombok
- Spring DevTools
- Maven

---

## 🚀 Étape 1 : Création du projet avec Spring Initializr
Le projet a été généré à l’aide de **Spring Initializr** :  
👉 https://start.spring.io

### Dépendances utilisées :
- Spring Data REST  
- Spring Data JPA  
- H2 Database  
- Lombok  
- Spring Boot DevTools  

Après génération, le projet a été téléchargé au format ZIP, extrait puis ouvert dans **IntelliJ IDEA**.

📌 *Spring Data REST permet d’exposer automatiquement les repositories comme des services RESTful, réduisant considérablement la création manuelle de contrôleurs.*


<img width="955" height="505" alt="tp11-1" src="https://github.com/user-attachments/assets/4ba48b9d-0bd6-48b7-bc68-678d74ed727f" />
<img width="948" height="503" alt="tp11-2" src="https://github.com/user-attachments/assets/68b56c25-44d7-459f-bb23-e1a4eafde08c" />
<img width="953" height="508" alt="tp11-3" src="https://github.com/user-attachments/assets/f8d01153-a5b5-4175-b667-625411c31269" />
<img width="958" height="506" alt="tp11-4" src="https://github.com/user-attachments/assets/fe935b00-ba3b-4134-8009-2018aeac91d7" />
<img width="956" height="507" alt="TP11-5" src="https://github.com/user-attachments/assets/7bc2a26a-fbc2-462e-9182-180cc70a026b" />
<img width="956" height="504" alt="TP11-6" src="https://github.com/user-attachments/assets/1e99705d-70ab-498a-95d0-7538d07a6e39" />


---

## ⚙️ Configuration de la base de données H2

```properties
# Configuration de la source de données H2
spring.datasource.url=jdbc:h2:mem:banque
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=

spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# Activer la console H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Configuration Hibernate
spring.jpa.hibernate.ddl-auto=update

# Configuration du serveur
server.port=8082

# Chemin de base des APIs Spring Data REST
spring.data.rest.base-path=/api






