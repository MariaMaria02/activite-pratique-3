# TP3 – Application Web Spring MVC avec Thymeleaf et Spring Security

**Réalisé par :** Habbouba Maria

## 📋 Description

Ce TP consiste à développer une **application web complète** de gestion de produits avec **Spring Boot**, **Thymeleaf** pour le rendu des vues côté serveur, et **Spring Security** pour sécuriser l'accès aux différentes fonctionnalités selon le rôle de l'utilisateur (authentification, autorisation, gestion des rôles USER/ADMIN).

## 🛠️ Technologies utilisées

- Java / Spring Boot
- Spring MVC
- Thymeleaf (+ Layout Dialect, Spring Security extras)
- Spring Security
- Spring Data JPA
- Base de données H2 / MySQL
- Maven

## 📁 Structure du projet

```
tp3-webapp/
├── src/main/java/ma/enset/
│   ├── controllers/        → AuthController, ProductController
│   ├── entities/            → Product
│   ├── repositories/        → ProductRepository
│   └── security/             → SecurityConfig (configuration Spring Security)
└── src/main/resources/
    ├── application.properties
    └── templates/
        ├── layout/           → Template global (template.html)
        ├── products/         → Liste et formulaire produits (list.html, form.html)
        └── security/         → Pages login et erreur d'accès (login.html, 403.html)
```

## ⚙️ Concepts clés

- **Architecture MVC** avec Spring Boot et moteur de templates Thymeleaf
- **Authentification** par formulaire (`formLogin`) avec utilisateurs en mémoire (`InMemoryUserDetailsManager`)
- **Encodage des mots de passe** avec `BCryptPasswordEncoder`
- **Autorisation basée sur les rôles** : restrictions d'accès (ex : suppression/ajout réservés aux administrateurs)
- Gestion des pages d'erreur (403 - Accès refusé)
- Intégration de `thymeleaf-extras-springsecurity6` pour afficher conditionnellement des éléments selon le rôle dans les vues HTML

## 👤 Utilisateurs de test

| Utilisateur | Mot de passe | Rôle(s) |
|---|---|---|
| user1 | 1234 | USER |
| user2 | 1234 | USER |
| admin | 1234 | USER, ADMIN |

## ▶️ Exécution

```bash
cd tp3-webapp
mvn spring-boot:run
```

Accès à l'application : `http://localhost:8080/products`


