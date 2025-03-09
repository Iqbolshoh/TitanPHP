# TitanPHP Framework

## Introduction
TitanPHP is a lightweight, high-performance PHP framework inspired by Laravel. It is designed to be fast, secure, and scalable while maintaining simplicity and ease of use. TitanPHP follows the **MVC (Model-View-Controller)** architecture and includes robust features like **routing, middleware, ORM, request handling, and security mechanisms**.

## Key Features
- **MVC Architecture** – Clean separation of concerns with Controllers, Models, and Views.
- **Routing System** – Inspired by Laravel, allowing easy URL handling.
- **ORM (Object-Relational Mapping)** – Database interaction using an Eloquent-like ORM.
- **Middleware Support** – Secures requests with authentication and authorization layers.
- **Blade or Twig Template Engine** – Dynamic rendering for frontend views.
- **Security Features** – Built-in protection against XSS, CSRF, and SQL Injection.
- **Environment Configuration (.env)** – Secure and flexible application settings.
- **Storage System** – Logging and caching mechanisms for better performance.
- **Unit Testing Support** – Framework includes a dedicated testing environment.

## File Structure
```
/TitanPHP
│── /app
│   ├── /Controllers        # MVC Controllers
│   ├── /Models             # ORM Model classes
│   ├── /Middleware         # Middleware for authentication and security
│   ├── /Views              # Blade or Twig templates
│
│── /bootstrap
│   ├── app.php             # Framework bootstrapping file
│
│── /config
│   ├── database.php        # Database configuration
│   ├── app.php             # General framework settings
│
│── /core
│   ├── Router.php          # Routing system
│   ├── Request.php         # HTTP request handling
│   ├── Response.php        # Response handling
│   ├── Database.php        # ORM and database connection
│   ├── Middleware.php      # Middleware handling
│   ├── Titan.php           # Core framework file
│
│── /public
│   ├── index.php           # Entry point
│
│── /routes
│   ├── web.php             # Web routes
│   ├── api.php             # API routes
│
│── /storage
│   ├── logs                # Log files
│   ├── cache               # Cached data
│
│── /tests
│   ├── ExampleTest.php     # Test directory
│
│── .env                    # Environment variables
│── .htaccess               # Apache configurations
│── composer.json           # PHP dependencies
│── README.md               # Framework documentation
```

## Installation
To install TitanPHP, follow these steps:
```sh
# Clone the repository
git clone https://github.com/your-repo/titanphp.git
cd titanphp

# Install dependencies
composer install

# Set up the environment file
cp .env.example .env

# Generate the application key
php artisan key:generate

# Migrate the database
php artisan migrate
```

## Routing Example
TitanPHP supports simple and expressive routing similar to Laravel:
```php
use Core\Router;

Router::get('/', function() {
    return 'Welcome to TitanPHP!';
});

Router::post('/login', 'AuthController@login');
```

## Middleware Example
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

## Database Example (ORM)
TitanPHP includes an ORM similar to Laravel's Eloquent:
```php
namespace App\Models;

use Core\Database;

class User extends Database {
    protected $table = 'users';
}

// Fetch users
$users = User::all();
```

## Contribution
If you would like to contribute to TitanPHP, feel free to submit a pull request or report an issue.

## License
TitanPHP is open-source and licensed under the MIT License.