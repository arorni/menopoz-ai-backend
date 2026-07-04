# Menopoz AI Backend - Milestone 1

## Setup

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Create `.env` from `.env.example`:

```env
DATABASE_URL=postgresql://postgres:your_password@localhost:5432/menopoz_ai
SECRET_KEY=change_this_to_a_long_random_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
```

Create PostgreSQL database:

```sql
CREATE DATABASE menopoz_ai;
```

Run server:

```bash
uvicorn app.main:app --reload
```

Open Swagger UI:

```text
http://127.0.0.1:8000/docs
```

## APIs

- GET `/health`
- POST `/auth/register`
- POST `/auth/login`
- GET `/auth/me`
