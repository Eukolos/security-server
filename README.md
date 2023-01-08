# security-server
Spring Security 6

### 🔨 Run the App

#### Maven

<b>1 )</b> Download your project from this link shown below
```
    git clone https://github.com/Eukolos/security-server.git
```

<b>2 )</b> Go to the project's home directory shown below
```
    cd security-server
```

<b>3 )</b> Create native image though this command shown below
```
    mvn -Pnative spring-boot:build-image
```

<b>4 )</b> Run the project though this command shown below
```
    docker-compose up
```

### Used Dependencies
* Core
    * Spring
        * Spring Boot 3
        * Spring Security 6
        * Spring Web
    * Jwt
        * Jwt Api
        * Jwt Impl
        * Jwt Jackson
* Postgresql
* Docker
* GraalVM CE Java 17-22.3.0

### Registration

```
POST api/v1/post/auth/register
Accept: application/json
Content-Type: application/json
{
    "firstname":"emin",
    "lastname":"aksoy",
    "email":"emin@gmail.com",
    "password": "123456"
}
RESPONSE: HTTP 201 (CREATED)
Content: String (JWToken)
Location header: http://localhost:8080/api/v1/auth/register
```

### Authenticate

```
POST api/v1/post/auth/authenticate
Accept: application/json
Content-Type: application/json
{
    "email":"emin@gmail.com",
    "password": "123456"
}
RESPONSE: HTTP 200 (OK)
Content: String (JWToken)
Location header: http://localhost:8080/api/v1/auth/authenticate
```

### Authenticate

```
GET /api/v1/demo-controller
Accept: application/json
Content-Type: application/json
AuthHeader: String (Valid JWToken)
RESPONSE: HTTP 200 (OK)
{
    "hello"
}
Location header: http://localhost:8080/api/v1/demo-controller
```

### Resource

- [Spring Boot 3 & Spring Security 6 Tutorial](https://www.youtube.com/watch?v=BVdQ3iuovg0&ab_channel=BoualiAli)
- [Spring Security 6 Releases](https://github.com/spring-projects/spring-security/releases)
