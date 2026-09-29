# Jobs Portal (PHP + MySQL)

A jobs/careers website built with PHP and MySQL, containerized with Docker.
Includes a public-facing site (job listings, applications, CVs, contact)
and an admin panel (manage jobs, categories, clients, staff, applicants).

## What it does

**Public site:**
- Browse job listings by department (IT, Sales, HR)
- View job details and apply with a CV upload
- Careers and contact pages

**Admin panel:**
- Add/edit/delete jobs, categories, clients, and staff
- View applicants and enquiries
- Client login

## Tech used

- PHP 8 (php:fpm-alpine)
- MySQL / MariaDB
- Nginx (web server)
- phpMyAdmin (database management UI)
- Docker & Docker Compose

## How to run it

1. Make sure Docker Desktop is installed and running.
2. Clone this repo and open a terminal in the project folder.
3. Start everything:
   ```
   docker-compose up -d
   ```
4. Import the database schema:
   - Open phpMyAdmin at [http://localhost:8080](http://localhost:8080)
   - Log in and import `websites/import.sql`
5. Visit the site:
   - Public site: [http://localhost](http://localhost)
   - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

## Project structure

| Path | What it is |
|---|---|
| `websites/jobs/public/` | Main jobs site (public pages + admin panel) |
| `websites/default/public/` | Default/placeholder site |
| `websites/import.sql` | Database schema and seed data |
| `docker-compose.yml` | Defines the nginx, PHP, MySQL, and phpMyAdmin containers |
| `PHP.Dockerfile` | PHP container setup |
| `nginx.conf` | Web server configuration |
