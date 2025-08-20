# Installation Guide

## Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

## Step-by-Step Installation

1. **Create Virtual Environment**
```bash
python -m venv venv
```

3. **Activate Virtual Environment**
- Windows:
```bash
venv\Scripts\activate
```
- Linux/Mac:
```bash
source venv/bin/activate
```

4. **Install Dependencies**
```bash
pip install Django==4.2.5 django-crispy-forms==2.0 crispy-bootstrap4==2022.1 django-jazzmin django-htmx==1.16.0 pytz==2021.3 python-dateutil==2.8.2 autopep8==1.6.0
```

5. **Configure Database**
```bash
python manage.py makemigrations
python manage.py migrate
```

6. **Create Superuser**
```bash
python manage.py createsuperuser
```

7. **Run Development Server**
```bash
python manage.py runserver
```

## Configuration

### Settings
The main settings are in `DjangoEHR/settings.py`:
- Database configuration
- Static files
- Templates
- Installed apps
- Middleware

### Environment Variables
Create a `.env` file in the root directory with:
```
DEBUG=True
SECRET_KEY=your-secret-key
```

## Troubleshooting

### Common Issues

1. **Database Migration Issues**
```bash
python manage.py migrate --run-syncdb
```

2. **Static Files Not Loading**
```bash
python manage.py collectstatic
```

3. **Dependencies Conflicts**
```bash
pip install -r requirements.txt --upgrade
```
