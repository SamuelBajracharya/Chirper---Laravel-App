# Chirper

Chirper is a small social feed built while learning Laravel. Users can create accounts, sign in, publish short messages called chirps, and manage their own posts.

The project is intentionally simple and is useful as a place to practice Laravel fundamentals with a real, working feature set.

## What I am learning

- Laravel routing and controller actions
- Blade views and reusable components
- Authentication, registration, and middleware
- Eloquent models and relationships
- Database migrations and seeders
- Form validation and authorization policies
- Vite, Tailwind CSS, and frontend asset building
- Feature and unit testing with PHPUnit

## Features

- User registration and login
- Authenticated logout
- Public chirp feed
- Create, edit, and delete your own chirps
- Per-user chirp relationships
- Seeded users and sample chirps for local development

## Requirements

- PHP 8.3 or newer
- Composer
- Node.js and npm
- A database supported by Laravel; the project is configured to work with SQLite by default

## Installation

Clone the repository and enter the project directory:

```bash
git clone <repository-url>
cd chirper
```

Install the PHP and JavaScript dependencies, create the environment file, generate the application key, run migrations, and build the frontend assets:

```bash
composer run setup
```

If you are setting the project up manually, the equivalent commands are:

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
npm install
npm run build
```

On Windows PowerShell, use `Copy-Item .env.example .env` instead of `cp .env.example .env`.

## Seed sample data

To add the sample users and chirps:

```bash
php artisan db:seed --class=ChirpSeeder
```

The seeded users use the password `password` and the following email addresses:

- `alice@example.com`
- `bob@example.com`
- `charlie@example.com`

Do not use these credentials in a production application.

## Run the application

Start Laravel and Vite together with:

```bash
composer run dev
```

Then open [http://localhost:8000](http://localhost:8000) in your browser. If your local Laravel setup uses a different port, use the URL shown in the terminal.

To run the frontend dev server separately:

```bash
npm run dev
```

## Testing

Run the test suite with:

```bash
composer run test
```

The tests are located in the `tests/Feature` and `tests/Unit` directories.

## Useful commands

```bash
php artisan route:list       # Display registered routes
php artisan migrate:fresh --seed
php artisan tinker            # Explore the application interactively
./vendor/bin/pint             # Format PHP files
```

On Windows, use `vendor\\bin\\pint.bat` if the shell does not run the Unix-style command.

## Project structure

| Directory | Purpose |
| --- | --- |
| `app/Http/Controllers` | Authentication and chirp request handling |
| `app/Models` | `User` and `Chirp` Eloquent models |
| `app/Policies` | Authorization rules for chirps |
| `database/migrations` | Database table definitions |
| `database/seeders` | Sample data for local development |
| `resources/views` | Blade pages and components |
| `resources/css` and `resources/js` | Frontend source files |
| `routes/web.php` | Web routes for the application |
| `tests` | Feature and unit tests |

## Learning resources

- [Laravel Documentation](https://laravel.com/docs)
- [Laravel Learn](https://laravel.com/learn)
- [Laracasts](https://laracasts.com)

## License

This learning project is open-sourced under the [MIT license](https://opensource.org/licenses/MIT).
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

In addition, [Laracasts](https://laracasts.com) contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

You can also watch bite-sized lessons with real-world projects on [Laravel Learn](https://laravel.com/learn), where you will be guided through building a Laravel application from scratch while learning PHP fundamentals.

## Agentic Development

Laravel's predictable structure and conventions make it ideal for AI coding agents like Claude Code, Cursor, and GitHub Copilot. Install [Laravel Boost](https://laravel.com/docs/ai) to supercharge your AI workflow:

```bash
composer require laravel/boost --dev

php artisan boost:install
```

Boost provides your agent 15+ tools and skills that help agents build Laravel applications while following best practices.

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
