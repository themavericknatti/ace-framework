# ⚡ Ace PHP MVC Framework — Skeleton Application

[![PHP Version](https://img.shields.io/badge/PHP-8.2%2B-blue.svg)](https://php.net)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Core Library](https://img.shields.io/badge/Powered%20By-acex%2Fcore-indigo.svg)](https://github.com/themavericknatti/ace)

The official application starter skeleton for the **Ace PHP MVC Framework**. Ace provides a modern, fast, and structured foundation for building web applications and REST APIs in PHP 8.2+ without bloated dependencies.

---

## 🚀 Quick Start

### 1. Create a New Project

You can scaffold a new project using Composer:

```bash
composer create-project acex/ace-framework my-app
cd my-app
```

Or clone this repository directly:

```bash
git clone https://github.com/themavericknatti/ace-framework.git my-app
cd my-app
composer install
```

### 2. Configure Environment

Copy the example environment configuration (automatically handled when using `composer create-project`):

```bash
cp .env.example .env
```

Open `.env` and set your database credentials:

```ini
APP_NAME="Ace Application"
APP_ENV=development
APP_DEBUG=true
APP_URL="http://localhost:8000"

DB_HOST=127.0.0.1
DB_PORT=3306
DB_NAME=ace_db
DB_USER=root
DB_PASS=
```

### 3. Run Database Migrations

Apply the initial schema:

```bash
php ace migrate
```

### 4. Start the Development Server

Launch the built-in development server:

```bash
php ace serve
```

Your application is now running at **[http://localhost:8000](http://localhost:8000)**!

---

## 📁 Directory Structure

```text
ace-framework/
├── app/
│   ├── Controllers/       # HTTP Controllers (e.g. HomeController.php)
│   ├── Jobs/              # Asynchronous / Queued background jobs
│   ├── Middlewares/       # HTTP & Route Middlewares
│   ├── Models/            # Active Record database models (e.g. User.php)
│   ├── Repositories/      # Data access layer
│   ├── Requests/          # FormRequest validation classes
│   └── Services/          # Domain business logic layer
├── config/
│   ├── app.php            # Core application configuration
│   ├── cors.php           # CORS middleware settings (React, Vue, mobile apps)
│   ├── database.php       # PDO connection & database configuration
│   ├── payment.php        # Unified payment gateway configurations
│   ├── settings.json      # Dynamic settings
│   └── templates.php      # Multi-template engine configuration
├── migrations/            # Version-controlled database migrations
├── public/                # Public web document root (pointed to by web servers)
│   ├── index.php          # Front Controller (Application entry point)
│   ├── .htaccess          # Apache rewrite rules
│   └── uploads/           # User file upload directory
├── routes/
│   ├── web.php            # Web routes (sessions, CSRF, template rendering)
│   └── api.php            # RESTful API routes (stateless, CORS, API Key / Bearer auth)
├── seeds/                 # Database seeders
├── storage/               # Application runtime storage
│   ├── cache/             # Rate-limiter & response cache
│   ├── framework/         # Maintenance down status & temp files
│   ├── logs/              # Application error & audit logs
│   └── views/             # Compiled template cache
├── tests/                 # Automated test suite
│   ├── Feature/           # Feature & integration tests
│   └── Unit/              # Unit tests
├── views/                 # Presentation layer (layouts, templates, errors)
├── .env.example           # Example environment file
├── .gitignore             # Standard git ignore definitions
├── .htaccess              # Root security and rewrite rules for shared hosting
├── ace                    # Ace CLI Command Runner executable
├── composer.json          # Project Composer manifest
└── GUIDE.md               # Comprehensive architecture & developer guide
```

---

## 🛠️ Ace CLI Commands

The included `ace` executable provides helpful CLI commands for development:

| Command | Description |
| :--- | :--- |
| `php ace serve` | Start local PHP development server at localhost:8000 |
| `php ace migrate` | Execute pending database migrations |
| `php ace migrate:rollback` | Roll back the most recent migration batch |
| `php ace migrate:status` | Check status of all migrations |
| `php ace db:seed` | Run database seeders |
| `php ace make:controller <Name>` | Generate a new Controller class |
| `php ace make:model <Name> -m` | Generate a new Model and migration |
| `php ace make:migration <name>` | Generate a new migration file |
| `php ace make:seeder <Name>` | Generate a new seeder class |
| `php ace make:middleware <Name>` | Generate a custom HTTP middleware |
| `php ace make:job <Name>` | Generate a new queued background job |
| `php ace make:request <Name>` | Generate a FormRequest validation class |
| `php ace make:repository <Name>` | Generate a Repository class |
| `php ace make:service <Name>` | Generate a Service business logic class |
| `php ace queue:work` | Run the background queue worker process |
| `php ace tinker` | Start interactive CLI console shell |
| `php ace down` / `php ace up` | Put application into or out of maintenance mode |

---

## 🧪 Testing

Run automated tests using PHPUnit:

```bash
composer test
# or
vendor/bin/phpunit
```

---

## 📖 Developer Documentation

For complete framework documentation, coding standards, layer responsibilities, and architecture guidelines, please consult:
- [GUIDE.md](GUIDE.md) — Comprehensive Ace Framework Architecture & Developer Guide
- [how-to-upload.md](how-to-upload.md) — Shared Hosting & cPanel Deployment Guide

---

## 📦 Core Engine & Ecosystem

- **Framework Core**: [`acex/core`](https://github.com/themavericknatti/ace)
- **Application Skeleton**: [`acex/ace-framework`](https://github.com/themavericknatti/ace-framework)

## 📄 License

The Ace PHP MVC Framework is open-sourced software licensed under the [MIT license](LICENSE).
