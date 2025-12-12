# CampusTrack - Secure Backend (JWT + BCrypt + MySQL-ready)

This backend includes:
- BCrypt password hashing
- JWT authentication (login/register return JWT)
- MySQL-ready config (update credentials in application.properties)
- H2 removed; use MySQL locally for persistence

## Setup

1. Create MySQL database (see db/setup.sql)
2. Update `src/main/resources/application.properties` if you changed MySQL creds
3. Build and run:
   - `mvn clean package`
   - `mvn spring-boot:run`
4. Auth routes (no token required):
   - POST /api/auth/register  { "username","password","fullName" }
   - POST /api/auth/login     { "username","password" }
5. Protected endpoints require header:
   `Authorization: Bearer <token>`

