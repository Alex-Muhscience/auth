# Auth

A robust and extensible authentication library for PHP.

## Features

- **User Authentication**: Secure user login and logout functionality.
- **Password Management**: Secure password hashing and verification.
- **Session Handling**: Manage user sessions with best practices.
- **Extensible**: Easily integrate custom authentication methods.
- **Lightweight**: Minimal dependencies, easy to integrate into any PHP project.

## Installation

Clone the repository or add it as a submodule to your project:

```bash
git clone https://github.com/Alex-Muhscience/auth.git
```

Or install via Composer (if available):

```bash
composer require alex-muhscience/auth
```

## Usage

### Basic Example

```php
require 'vendor/autoload.php';

// Initialize the Auth system
$auth = new Auth();

// Register a new user
$auth->register('username', 'password');

// Login
if ($auth->login('username', 'password')) {
    echo "Login successful!";
} else {
    echo "Invalid credentials.";
}

// Logout
$auth->logout();
```

### Password Reset

```php
if ($auth->resetPassword('username', 'newpassword')) {
    echo "Password reset successful!";
}
```

## Configuration

You can configure the authentication system by editing the config file:

```php
$config = [
    'session_timeout' => 3600, // seconds
    'hash_algo' => PASSWORD_DEFAULT,
    // Add other configuration options as needed
];

$auth = new Auth($config);
```

## Folder Structure

- `/src` - Main library code
- `/tests` - Unit tests
- `/examples` - Example usage scripts

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements or bug fixes. Make sure to write tests for any new features.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Author

[Alex-Muhscience](https://github.com/Alex-Muhscience)
