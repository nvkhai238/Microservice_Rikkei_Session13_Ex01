# Session 13 - Bai 1: Identity va BCrypt

Yeu cau JDK 21 va Docker. Chay `docker compose up -d --wait`, sau do `./gradlew :identity-service:bootRun`. PostgreSQL tao database `identity_db` o cong 5436. Cau hinh qua `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASSWORD`.

Dang ky: `POST http://localhost:8080/api/auth/register` voi JSON `{"username":"alice","password":"password123"}`. API tra 201, id va role USER, khong tra password. Mat khau luu trong cot `password_hash` duoi dang BCrypt. Dang ky trung username tra 409.
