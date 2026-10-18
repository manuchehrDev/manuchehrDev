# Привет 👋 Я Манучехр - Java Backend Developer (Junior)

Учебные и командные проекты в рамках bootcamp **«21 School»** (School 21 / Open­sso).  
Фокус — backend на **Java / Spring**, REST API, **PostgreSQL**, **JWT-авторизация**, микросервисы, Docker и CI/CD.

- 🔭 Сейчас углубляюсь в Spring Security, gRPC и событийно-ориентированную архитектуру
- 💬 Спроси меня про Spring MVC, JPA, JWT, PostgreSQL и Nginx
- 📫 Связаться: `baxbyman@gmail.com` · [Telegram](@manuchehrdev) · [LinkedIn](https://www.linkedin.com/in/manuchehr-barotov-5aaa08444/)

---

## 🛠 Стек

**Языки**
![Java](https://img.shields.io/badge/Java%2018-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Backend**
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA%2FHibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Базы данных**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)

**Инфраструктура и инструменты**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black)

---

## 🚀 Ключевые проекты

### 🎮 Tic-Tac-Toe Web App — Spring MVC, слоистая архитектура, Minimax
- Gradle-проект Java 18 (Kotlin DSL), слои `web` / `domain` / `datasource` / `di`.
- REST `POST /game/{UUID}`, DTO и мапперы, потокобезопасное хранилище, DI через Spring Configuration.
- Алгоритм «Минимакс», поддержка нескольких игр одновременно, обработка ошибок некорректного хода.

### 🔐 Tic-Tac-Toe + PostgreSQL + JWT
- **PostgreSQL + JPA**: подключение, `CrudRepository`, пользователи с UUID.
- **Basic Auth → JWT**: `JwtProvider` (`jjwt`) с access/refresh-токенами, `JwtAuthentication`, `JwtUtil`, `SecurityContextHolder`.
- `AuthFilter` на `GenericFilterBean`, `SecurityFilterChain`, роли (`GrantedAuthority`).
- История завершённых игр и таблица лидеров (top-N) с защищёнными endpoint’ами.

### 🛒 ShopAPI — REST-сервис магазина бытовой техники
- PostgreSQL в нормальных формах: `client`, `product`, `supplier`, `images`, `address`, внешние ключи, UUID.
- RESTful CRUD `/api/v1/...`: клиенты, товары, поставщики, изображения; пагинация `limit`/`offset`.
- DTO и мапперы, паттерн **Repository/DAO**, валидация (`400`/`404`), отдача бинарных данных.
- **OpenAPI/Swagger**: комментарии, примеры, Swagger UI по `/swagger/index.html`.

### 🧩 Микросервисы — gRPC, брокеры, кэш, шардирование
- **gRPC-сервис авторизации** (`.proto`, HTTP/2) со своей БД: JWT, хэширование с солью, middleware и кастомные атрибуты.
- **RabbitMQ/Kafka + gateway** → обновление данных и рассылка по **WebSockets/SSE**.
- **Redis** для кэша фото; **шардирование** фото по 4 БД PostgreSQL по первому символу UUID.
- **OAuth 2.0 через Google** (client_id/secret из env), делегирование аутентификации.

### 🐾 Pet Info / Java Fundamentals
- ООП: абстрактные классы, интерфейсы, полиморфизм, дженерики, `List`, собственный итератор.
- Stream API и лямбды, многопоточность (`Thread`/`Executor`), `TimeUnit`.
- Алгоритмы, рекурсия, массивы, файловый ввод-вывод, валидация ввода.

### 🗄 SQL / PostgreSQL (учебные модули)
- `SELECT` / `JOIN` / `UNION` / `EXCEPT`, CTE, `generate_series`, views и materialized views.
- Индексы: BTree, функциональные, частичные, покрывающие, `EXPLAIN ANALYZE`.
- Транзакции и уровни изоляции (`READ COMMITTED`, `REPEATABLE READ`, `SERIALIZABLE`), deadlock.
- Триггеры и PL/pgSQL-функции, аудит, DWH/ETL, рекурсивные запросы (TSP).

### ⚙️ Инфраструктура
- **Nginx**: reverse proxy, маршрутизация `/api` → `/api/v1`, статика, upstream-балансировка, кэш, gzip, HTTPS (openssl).
- **Docker / Docker Compose**: свой образ (nginx + мини-сервер на C/FastCGI), `docker build/cp/export/import`, Dockle.
- **GitLab CI/CD**: `.gitlab-ci.yml`, сборка, `clang-format`, интеграционные тесты, деплой через `ssh`/`scp`, Telegram-уведомления.

### 🎲 Дополнительно
- **Roguelike (Java)** — консольная 2D-игра, процедурная генерация уровней, пошаговый бой, инвентарь, сохранение в JSON, многослойная архитектура.
- **Kotlin Fundamentals** — коллекции, `sequences`, функции расширения, файловый ввод-вывод.
- **C / C++** — `s21_string+`, `s21_decimal`, `s21_matrix`, `BrickGame Tetris`, `s21_matrix+` (C++20, GTest).

---

## 📊 GitHub Stats

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=transparent&hide_border=true&count_private=true" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=transparent&hide_border=true&langs_count=8" />
</p>

---

## 📫 Контакты

- 📧 Email: `baxbyman@gmail.com`
- 💬 Telegram: [@manuchehrdev](https://t.me/manuchehrdev)
- 💼 LinkedIn: [linkedin.com/in/manuchehr-barotov](https://www.linkedin.com/in/manuchehr-barotov-5aaa08444/)

> Открыт к предложениям по **Java Backend (Junior)** — Spring, REST, PostgreSQL, микросервисы.#   m a n u c h e h r D e v  
 