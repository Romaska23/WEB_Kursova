# Aurora SkillGraph

Веб-застосунок для побудови персональних графів навичок з AI-генерацією дорожніх карт.

## Вимоги

- Python 3.10+
- Docker & Docker Compose
- Gemini API ключ ([отримати тут](https://aistudio.google.com/app/apikey))

## Запуск

### 1. Клонування репозиторію

```bash
git clone <repo-url>
cd WEB_Kursova
```

### 2. Налаштування змінних середовища

Скопіюйте `.env.example` у `.env` та заповніть значення:

```bash
cp .env.example .env
```

Відредагуйте `.env`:

```
SECRET_KEY='django-insecure-your-secret-key-here'
DEBUG=True
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=5432
GEMINI_API_KEY=your_gemini_api_key
```

### 3. Створення та активація віртуального середовища

```powershell
py -m venv venv
.\venv\Scripts\Activate.ps1
```

### 4. Встановлення залежностей

```bash
pip install -r requirements.txt
```

### 5. Запуск бази даних (PostgreSQL через Docker)

```bash
docker-compose up -d
```

### 6. Міграції

```bash
python manage.py migrate
```

### 7. Запуск сервера

```bash
python manage.py runserver
```

Відкрийте у браузері: [http://localhost:8000](http://localhost:8000)

### 8. Створення адміністратора (опційно)

```bash
python manage.py createsuperuser
```

Адмін-панель: [http://localhost:8000/admin](http://localhost:8000/admin)

### Зупинка

```bash
docker-compose down
```
