# Snippetbox

Snippetbox is a web application for creating, sharing, and managing code snippets. It was built using Go, following the "Let's Go" book by Alex Edwards.

## Features

Authentication. Users can register and sign in.
Protected endpoints. Only signed-in users can create snippets.
RESTful routing.
Middleware.
MySQL database.
SSL/TLS web server using HTTP 2.0.
Generated HTML via Golang templates.
CRSF protection.
## Getting Started

### Prerequisites

Go 1.16+
MySQL server
### Installation

Clone the Repository:

```bash
git clone https://github.com/KemalBekir/snippetbox.git
cd snippetbox
```

Set Up MySQL:

```sql
CREATE DATABASE snippetbox CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'snippetbox'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON snippetbox.* TO 'snippetbox'@'localhost';
mysql -u snippetbox -p snippetbox < ./sql/schema.sql
```

Run the Application:

```bash
go run ./cmd/web
```

Visit `http://localhost:4000\`.

### Testing

```bash
go test -v ./...
```

## License

Licensed under the MIT License.

## Acknowledgments

Built following the "Let's Go" book by Alex Edwards.
