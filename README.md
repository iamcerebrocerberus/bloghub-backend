# BlogHub Backend

A Django REST API backend for a blog platform built with Django 5.2 and Django REST Framework.

## Project Structure

```
bloghub-backend/
├── account/          # User account management app
├── config/           # Django project configuration
├── core/             # Core application functionality
├── manage.py         # Django management script
├── requirements.txt  # Python dependencies
├── pytest.ini       # Testing configuration
└── .env.example      # Environment variables template
```

## Requirements

- Python 3.8+
- pip
- Virtual environment (recommended)

## Quick Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd bloghub-backend
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` file with your configuration:
   ```
   DEBUG=True
   DJANGO_SECRET=your-secret-key-here
   DJANGO_SETTINGS_MODULE=config.settings_dev
   ```

5. **Run migrations**
   ```bash
   python manage.py migrate
   ```

6. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Start the development server**
   ```bash
   python manage.py runserver
   ```

The API will be available at `http://127.0.0.1:8000/`

## Key Dependencies

- **Django 5.2.6** - Web framework
- **Django REST Framework 3.16.1** - API framework
- **django-environ 0.12.0** - Environment variable management
- **drf-spectacular 0.28.0** - API documentation
- **pytest 8.4.2** - Testing framework
- **pytest-django 4.11.1** - Django testing integration

## Development

### Running Tests

```bash
pytest
```

### Database

The project uses SQLite by default for development. The database file is `db.sqlite3`.

### Settings

- Development: `config.settings_dev`
- Production: `config.settings_prod`
- Base: `config.settings`

## Apps

- **account**: User authentication and profile management
- **core**: Core application functionality and shared utilities

## Environment Variables

Create a `.env` file based on `.env.example`:

- `DEBUG`: Enable/disable debug mode
- `DJANGO_SECRET`: Django secret key for cryptographic signing
- `DJANGO_SETTINGS_MODULE`: Settings module to use

## API Documentation

With drf-spectacular installed, API documentation should be available at:
- `/api/schema/` - OpenAPI schema
- `/api/docs/` - Swagger UI (if configured)

## Contributing

1. Create a virtual environment and install dependencies
2. Make your changes
3. Run tests with `pytest`
4. Ensure code follows project conventions
5. Submit a pull request

## License

[Add your license information here]