# Привет 👋

**Junior Backend Developer (C#)** · Екатеринбург. Разрабатываю серверные приложения, REST API, фоновые сервисы и клиент-серверные решения на платформе `.NET` с акцентом на надёжность, читаемость кода и понятную архитектуру.

* **Портфолио / сайт:** `https://bikmacs.github.io/`
* **GitHub:** `https://github.com/Bikmacs`
* **Telegram:** `@Macsonchikk`
* **Email:** `macsim.shmelev@yandex.ru`

---

## 🛠 Навыки и инженерные темы

Совмещаю практическую разработку в проектах и на практике с системной подготовкой к уровню `Junior+` по C#, `.NET`, базам данных, инфраструктуре и тестированию.

### Основной стек и практика
* **Языки и платформа:** C#, `.NET` (`.NET 9` / `.NET 10`), `ASP.NET Core` (`Web API`, `MVC`), `TypeScript`, `WPF`.
* **Базы данных и ORM:** `PostgreSQL`, `MS SQL Server`, `SQLite`, `Entity Framework Core`, проектирование схем, индексы и оптимизация запросов.
* **Асинхронность, real-time и интеграции:** `async/await`, `CancellationToken`, `REST API`, `Telegram Bot API` (`Webhook`, inline-клавиатуры), `SignalR` / `WebSocket`.
* **Брокеры, кэш и инфраструктура:** `IMemoryCache`, `Redis` (включая Lua-скрипты и паттерн *Fail-Open*), `RabbitMQ` (`MassTransit`), `YARP`, `Docker` и `Docker Compose`, `Linux VPS` (`Ubuntu LTS`), `Nginx`, `systemd`, `cron`, `Git`, `CI/CD` (`GitHub Actions`).
* **Тестирование:** модульные и интеграционные тесты (`NUnit`, `xUnit`, `Moq`).

### В активной проработке (план подготовки к Junior+)
* **Внутреннее устройство `.NET` и память:** устройство CLR, стек и управляемая куча, сборка мусора (`GC`), `IAsyncStateMachine`, `Span<T>`, борьба с аллокациями и *Cache Stampede*.
* **Архитектура и эксплуатация:** `Rich vs. Anemic Domain Model`, `Vertical Slice Architecture`, работа с `EF Core` без лишних обёрток-репозиториев, `Dapper`, `IExceptionHandler` + `ProblemDetails`, `Serilog` + `Seq`, `Channel<T>`, `WebApplicationFactory`.

---

## 🚀 Ключевые проекты

Три ключевых проекта охватывают защиту трафика и фоновую обработку событий, коммерческую full-stack разработку с деплоем на VPS и клиент-серверные приложения.

### 1. BotGuard — Anti-Abuse API Gateway
* **Репозиторий:** `https://github.com/Bikmacs/BotGuard`
* **Стек:** C#, `.NET 10`, `ASP.NET Core`, `YARP`, `Redis`, `RabbitMQ`, `MassTransit`, `PostgreSQL 17`, `Entity Framework Core`, `Docker`, `xUnit`, `Moq`, `GitHub Actions`
* **Что реализовано:** Event-driven архитектура защиты веб-сайтов от ботов, парсеров и «шумных» клиентов. Горячий путь (`BotGuard.Gateway` на базе `YARP`) проверяет `User-Agent`, чёрный список IP и `Rate Limit` (fixed window через `Redis` и Lua-скрипты) с поведением *Fail-Open*, а холодный путь (`BotGuard.BanConsumer`) асинхронно обрабатывает события через `RabbitMQ`, банит IP в `Redis` и сохраняет инциденты в `PostgreSQL`. После перехода на публикацию события только при первом нарушении за окно нагрузки в тесте достигнуто **+1 инцидент на 927 018 запросов**, `latency 3.43 ms` и `0 таймаутов` (против `32 308` инцидентов, `latency 912 ms` и `433` таймаутов до исправления).

### 2. Artema 31 — система онлайн-бронирования банкетного зала
* **Сайт:** `https://artema-31.ru`
* **Стек:** C#, `ASP.NET Core Web API` (`.NET 9`), `Entity Framework Core`, `SQLite`, `Scalar / OpenAPI`, `Telegram.Bot` (`Webhook` + inline-клавиатуры), `TypeScript` (`Vanilla TS`), `Vite`, `Linux VPS` (`Ubuntu LTS`), `Nginx`, `systemd`, `cron`
* **Что реализовано:** Коммерческий full-stack проект для автоматизации бронирования банкетного зала с интерактивным календарём занятости и двусторонним управлением заявками через Telegram-бота. Включает серверную часть (`Artema31.Backend`), модульные и интеграционные тесты (`Artema31.Backend.Tests`), клиентское приложение на TypeScript (`Artem31-frontend`) и продакшен-контур на VPS с `Nginx` (reverse proxy, SSL Let's Encrypt), `systemd` и автоматическим бэкапом `SQLite` по `cron`.

### 3. CafeSystem (`CafeSolution`) — система автоматизации кафе
* **Репозиторий:** `https://github.com/Bikmacs/CafeSystem`
* **Стек:** C#, `ASP.NET Core Web API`, `Entity Framework Core`, `WPF`, `SignalR`, `Docker Compose`
* **Что реализовано:** Клиент-серверная система автоматизации процессов кафе с `Backend API` и desktop-клиентом на `WPF` для сотрудников, поддержкой ролей и работой в реальном времени. Проект развивался с разделением сервисов, включая проработку отдельного сервиса чата на `SignalR` с группами комнат, `CORS`, настройкой портов и запуском через `Docker Compose`.

---

## 💼 Опыт и образование

* **Практикант Fullstack-разработчик — «Кнопка»** *(январь 2026 — май 2026, 5 месяцев)*: разрабатывал серверную часть на C# и `ASP.NET Core` для автоматизации финансовых процессов, проектировал API и работал с `PostgreSQL`. Реализовывал интеграции с Контур.Экстерн для отправки отчётности в ФНС, СФР и Росстат, работу с МЧД и обработку XML, вёл разработку на `TypeScript`, выполнял рефакторинг и оптимизацию запросов к БД, покрывал сервисы тестами на `NUnit` в рамках `CI/CD`.
* **Екатеринбургский колледж транспортного строительства** *(2026)*: специальность *«Информационные системы и программирование»* (`09.02.07`), демонстрационный экзамен.
