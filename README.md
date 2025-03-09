# 🌟 TitanPHP Framework

## 🚀 Introduction
TitanPHP is a **lightweight**, **high-performance** PHP framework inspired by Laravel. It is designed to be **fast**, **secure**, and **scalable**, while maintaining simplicity and ease of use. TitanPHP follows the **MVC (Model-View-Controller)** architecture and includes robust features like **routing**, **middleware**, **ORM**, **request handling**, and **security mechanisms**.

## ✨ Key Features
✅ **MVC Architecture** – Clean separation of concerns with Controllers, Models, and Views.  
✅ **⚡ Fast & Efficient Routing** – Inspired by Laravel, allowing easy URL handling.  
✅ **🔗 ORM (Object-Relational Mapping)** – Database interaction using an Eloquent-like ORM.  
✅ **🛡️ Middleware Support** – Secures requests with authentication and authorization layers.  
✅ **🎨 Blade or Twig Template Engine** – Dynamic rendering for frontend views.  
✅ **🔒 Security Features** – Built-in protection against XSS, CSRF, and SQL Injection.  
✅ **⚙️ .env Configuration** – Secure and flexible application settings.  
✅ **📁 Storage System** – Logging and caching mechanisms for better performance.  
✅ **🧪 Unit Testing Support** – Built-in testing environment for better code reliability.  

---

## 📂 File Structure
```
/TitanPHP
│── /app
│   ├── /Controllers        # 🎯 MVC Controllers
│   ├── /Models             # 🗄️ ORM Model classes
│   ├── /Middleware         # 🛡️ Middleware for authentication and security
│   ├── /Views              # 🎨 Blade or Twig templates
│
│── /bootstrap
│   ├── app.php             # ⚙️ Framework bootstrapping file
│
│── /config
│   ├── database.php        # 🗄️ Database configuration
│   ├── app.php             # ⚙️ General framework settings
│
│── /core
│   ├── Router.php          # 🔗 Routing system
│   ├── Request.php         # 📥 HTTP request handling
│   ├── Response.php        # 📤 Response handling
│   ├── Database.php        # 🗄️ ORM and database connection
│   ├── Middleware.php      # 🛡️ Middleware handling
│   ├── Titan.php           # 🏗️ Core framework file
│
│── /public
│   ├── index.php           # 🚪 Entry point
│
│── /routes
│   ├── web.php             # 🌎 Web routes
│   ├── api.php             # 🔌 API routes
│
│── /storage
│   ├── logs                # 📝 Log files
│   ├── cache               # 🚀 Cached data
│
│── /tests
│   ├── ExampleTest.php     # 🧪 Test directory
│
│── .env                    # 🔒 Environment variables
│── .htaccess               # ⚙️ Apache configurations
│── composer.json           # 📦 PHP dependencies
│── README.md               # 📜 Framework documentation
```

---

## 🔧 Installation
To install **TitanPHP**, follow these simple steps:
```sh
# 📥 Clone the repository
git clone https://github.com/your-repo/titanphp.git
cd titanphp

# 📦 Install dependencies
composer install

# ⚙️ Set up the environment file
cp .env.example .env

# 🔑 Generate the application key
php artisan key:generate

# 🗄️ Migrate the database
php artisan migrate
```

---

## 🌍 Routing Example
TitanPHP supports simple and expressive routing similar to Laravel:
```php
use Core\Router;

Router::get('/', function() {
    return '🚀 Welcome to TitanPHP!';
});

Router::post('/login', 'AuthController@login');
```

---

## 🛡️ Middleware Example
```php
namespace App\Middleware;

class AuthMiddleware {
    public function handle($request, $next) {
        if (!isset($_SESSION['user'])) {
            return redirect('/login');
        }
        return $next($request);
    }
}
```

---

## 🗄️ Database Example (ORM)
TitanPHP includes an **ORM** similar to Laravel's **Eloquent**:
```php
namespace App\Models;

use Core\Database;

class User extends Database {
    protected $table = 'users';
}

// Fetch users
$users = User::all();
```

---

## 📜 License
TitanPHP is **open-source** and licensed under the **MIT License**.  

🚀 Happy coding with **TitanPHP**! 🔥

---

## 🤝 Contribution

We welcome contributions! 🎉 If you’d like to help improve **TitanPHP**, feel free to submit a **pull request** or report an **issue** on GitHub.  

## 📬 Connect with Me  

💬 I love meeting new people and discussing tech, business, and creative ideas. Let’s connect! You can reach me on these platforms:

<div align="center">
    <table>
        <tr>
            <td>
                <a href="https://github.com/iqbolshoh">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg"
                        height="40" width="40" alt="GitHub" />
                </a>
            </td>
            <td>
                <a href="https://t.me/iqbolshoh_777">
                    <img src="https://github.com/gayanvoice/github-active-users-monitor/blob/master/public/images/icons/telegram.svg"
                        height="40" width="40" alt="Telegram" />
                </a>
            </td>
            <td>
                <a href="https://www.linkedin.com/in/iiqbolshoh/">
                    <img src="https://github.com/gayanvoice/github-active-users-monitor/blob/master/public/images/icons/linkedin.svg"
                        height="40" width="40" alt="LinkedIn" />
                </a>
            </td>
            <td>
                <a href="https://instagram.com/iqbolshoh_777" target="blank">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg"
                        alt="Instagram" height="40" width="40" />
                </a>
            </td>
            <td>
                <a href="https://wa.me/qr/22PVFQSMQQX4F1">
                    <img src="https://github.com/gayanvoice/github-active-users-monitor/blob/master/public/images/icons/whatsapp.svg"
                        height="40" width="40" alt="WhatsApp" />
                </a>
            </td>
            <td>
                <a href="https://x.com/iqbolshoh_777">
                    <img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" height="40"
                        width="40" alt="Twitter" />
                </a>
            </td>
            <td>
                <a href="mailto:iilhomjonov777@gmail.com">
                    <img src="https://github.com/gayanvoice/github-active-users-monitor/blob/master/public/images/icons/gmail.svg"
                        height="40" width="40" alt="Email" />
                </a>
            </td>
        </tr>
    </table>
</div>