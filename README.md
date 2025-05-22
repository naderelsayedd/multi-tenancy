# 🏢 Laravel 12 Multi-Tenancy SaaS App

A scalable **Multi-Tenant SaaS application** built with **Laravel 12** and **PHP 8.3**, powered by the [tenancyforlaravel](https://tenancyforlaravel.com/docs/v3/introduction/) package. This project provides an out-of-the-box setup for building robust multi-tenant platforms where each tenant has its own isolated database, routes, and resources.

---

## 🚀 Features

- 🔑 **Multi-Tenancy with Isolated Databases**  
  Each tenant has a dedicated database, offering data security and scalability.

- 🌐 **Central and Tenant Routing**  
  Separate routes and domains for central and tenant-specific logic.

- 🧩 **Modular Structure**  
  Clean and maintainable codebase using Laravel service providers and modules.

- ⚙️ **Tenant Aware Artisan Commands**  
  Automatically run artisan commands per tenant.

- 🧪 **Ready for Testing**  
  Set up with testing scaffolds for tenant-specific logic.

- 📈 **Scalable Architecture**  
  Ideal foundation for SaaS applications with growing user bases.

---

## 🧰 Tech Stack

- **Laravel 12**
- **PHP 8.3**
- **TenancyForLaravel v3**
- **MySQL / PostgreSQL** (configurable)
- **Composer**
- **Docker** (optional for local development)

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/naderelsayedd/multi-tenancy.git
cd multi-tenancy
```

### 2. Install Dependencies

```bash
composer install
```

### 3. Configure Environment

Copy the example environment file and set your credentials:

```bash
cp .env.example .env
php artisan key:generate
```

Update the `.env` file:

```env
APP_NAME="Laravel SaaS"
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=central
DB_USERNAME=root
DB_PASSWORD=your_password
```

### 4. Run Migrations

```bash
php artisan migrate
```

### 5. Install Tenancy Package

```bash
php artisan tenancy:install
```

### 6. Create Tenant

```bash
php artisan tenancy:tenant:create example.com
```

This will automatically set up a new tenant database and configure its environment.

### 7. Serve the Application

```bash
php artisan serve
```

Ensure your `/etc/hosts` or DNS is configured to handle tenant domains if needed (e.g., `example.localhost`).

---

## 🧪 Running Tests

```bash
php artisan test
```

---

## 👤 Author

**Nader Elsayed**  
GitHub: [@naderelsayedd](https://github.com/naderelsayedd)

---

## 📄 License

This project is open-source and available under the [MIT license](LICENSE).
