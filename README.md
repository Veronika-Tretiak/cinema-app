# Cinema-app 🎥

### 📜 Description
This is a simulation of cinema  service for reservation tickets, 
that supports registration, authentication and CRUD operations. It was written in Java and Spring.
All information is received in JSON format.
### ⚙️ Features
- This program supports two type of roles: 
ADMIN and USER. 
- Register or login
- Create and find movies
- Create and find available movie sessions
- Create shopping cart
- Add tickets to shopping cart
- Complete an order

| Roles   | Endpoints                                                                                                                                                                                                                                                           |
|:--------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `All`   | POST: /register                                                                                                                                                                                                                                                     |
| `Admin` | GET: /cinema-halls<br/>POST: /cinema-halls<br/>GET: /movies<br/>POST: /movies<br/>GET: /movie-sessions/available<br/>POST: /movie-sessions<br/>PUT: /movie-sessions/{id}<br/>DELETE: /movie-sessions/{id}<br/>GET: /users/by-email                                  |
| `User`  | GET: /cinema-halls<br/>GET: /movies<br/>GET: /movie-sessions/available<br/>GET: /orders<br/>POST: /orders/complete<br/>PUT: /shopping-carts/movie-sessions<br/>GET: /shopping-carts/by-user                                                                         |

### 🗄 Architecture
| Project structure |
| :-------- |
|`Presentation tier - Controllers`|
| `Application tier - Service` |
| `Data access tier - DAO` |

#### Database structure
![diagram](img/uml.png)

### 💻 Technologies
- JDK 17
- Spring 5.3.20
- Spring Security 5.6.10
- Hibernate 5.6.14
- [MySQL](https://www.mysql.com/) 8.0.22
- [Apache Tomcat](https://tomcat.apache.org/) 9.0.50
- [Apache Maven](https://maven.apache.org/) 3.3.2

### 🛠 Installation of the project:
- Clone this project from GitHub
- Create schema manually
- Configure /resources/db.properties
- Configure Tomcat server :
    - Edit configuration;
    - Tomcat Server -> Local
    - Deployment -> add -> artifact -> taxi-service:war exploded
        - Application context : /
    - Pres apply -> okay.

The program will create the first user automatically.
<br/>Role: ADMIN 
<br/>Email: admin@i.ua
<br/>Password: admin123 