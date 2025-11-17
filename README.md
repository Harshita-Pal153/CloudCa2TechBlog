

# TechBlog – Cloud-Deployed Technical Blogging Platform

TechBlog is a full-stack Java web application for creating, managing, and publishing technical blogs.
It supports user authentication, dynamic blog management, category-based browsing, and cloud-hosted storage.
The application is deployed using **Render** (hosting) and **Railway** (MySQL cloud database).

---

## Features

### User Features

* View latest and trending technology blogs
* Register and log in
* Create, edit, update, and delete blog posts
* Category-based blog filtering (Java, Python, Web Dev, AI, C++, etc.)
* Mark posts as favorite
* Bookmark posts
* View all posts in a structured layout

### Backend / System Features

* Java Servlets and JSP
* Hibernate ORM for database management
* Cloud-based MySQL database
* Session management (login state, authentication)
* Validations for form inputs
* MVC-structured application
* JDBC fallback usage where required

### Deployment Features

* Render hosting for the application
* Railway MySQL database for persistent cloud storage
* Dockerfile-based deployment using Tomcat
* Public production URL for live access

---

## Tech Stack

**Frontend:** JSP, HTML, CSS, Bootstrap, JavaScript
**Backend:** Java, Servlets, Hibernate, JDBC
**Database:** MySQL (Railway Cloud Database)
**Deployment:** Render (Hosting), Railway (Database), Docker, Tomcat 9

---

## System Architecture

### Modules

* User Authentication
* Blog Creation Module
* Blog Update & Delete
* Category Filtering
* Blog Display Engine
* Cloud DB Connector
* Session Handler

### Entities

#### User

* id
* name
* email
* password

#### Post

* id
* title
* content
* language
* date
* favorite
* bookmark

---

## Project Flow

1. User opens the homepage
2. Homepage displays latest blogs
3. User chooses to sign up or log in
4. After successful login, dashboard access is granted
5. User can add, edit, delete, or view blogs
6. All content is stored in the Railway cloud database
7. Render hosts and serves the entire application publicly

---

## Cloud Deployment Summary

### 1. Railway (MySQL Database)

* A cloud MySQL instance was created on Railway
* Connection details exported through environment variables
* Existing local schema imported into the Railway instance
* Hibernate configuration updated with Railway credentials

### 2. Render (Hosting)

* GitHub repository connected to Render
* Java environment configured with a Dockerfile
* WAR deployed via Tomcat base image
* Public URL generated after deployment

### 3. Dockerfile Used for Deployment

```
FROM tomcat:9-jdk11-openjdk
RUN rm -rf /usr/local/tomcat/webapps/*
COPY blog.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
```

---

## Live Website URL

```
https://cloudca2techblog.onrender.com/index.jsp
```

---

## Key Pages 
[Document link] (https://drive.google.com/file/d/1G3WuON1iTfNEOswEEOqy_Pa3CBD62yKD/view?usp=drive_link)

---

## Conclusion

This project demonstrates a complete implementation of a cloud-connected Java blogging system using JSP, Servlets, Hibernate, MySQL, Docker, Render, and Railway. It showcases production-style deployment, dynamic content management, and a fully functional technical blogging workflow.

