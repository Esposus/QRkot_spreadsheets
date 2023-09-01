# QRkot_spreadsheets

## Описание проекта

**QRkot spreadsheets** - Расширение для проекта QRKot, которое дает возможность формирования отчёта в гугл-таблице. В таблице должны быть закрытые проекты, отсортированные по скорости сбора средств — от тех, что закрылись быстрее всего, до тех, что долго собирали нужную сумму.

## Технологии
- Python 3.10
- FastAPI
- SQLAlchemy
- Google API
## Установка
1. Склонируйте репозиторий:
```
git clone git@github.com:Esposus/QRkot_spreadsheets.git
```
2. Cоздайте и активируйте виртуальное окружение:

```
python -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

    ```
    source venv/scripts/activate
    ```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

3. Создайте в корневой директории файл .env со следующим наполнением:

```
APP_TITLE=Кошачий благотворительный фонд
APP_DESCRIPTION=Сервис для поддержки котиков
DATABASE_URL=sqlite+aiosqlite:///./<название базы данных>.db
SECRET=<секретное слово>
FIRST_SUPERUSER_EMAIL=<email суперюзера>
FIRST_SUPERUSER_PASSWORD=<пароль суперюзера>
TYPE=service_account
PROJECT_ID=eminent-kit-397411
PRIVATE_KEY_ID=7c0f0c90ebaf2b6f2fe59c14798bb2fe2ff75c05
PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQC5LH9SZ6Km4YeZ\nzpMsu/+kwDXO22Pe3cUrhGzi3BcwSuc4p7vjbwMATWPnySxHE415/qEv5e1PZtc7\n/L6P5LYler0dxWWAtp1OBXx1wLeXeqZyBH3o2IY7Q9p17BqNRvU4PzR5fdz+pp55\nury8Gn4Nzv4sW4SIYXddxk2wMzvspyNHAJbYv1DNYVnf3g/dNbv1rHUliOmz9IEj\nFBJqK39JfRZRfeBTWm/ZzRzJrscxZJxdNg3tIsk/3jFUb0RIt3ZZR64tXwLjEJNL\nHHdHuVnLo0VdKYbrmJbH9HPWp1zWKIo8Z+l9RNfmyDJ/6UFQAosPfAs86PIvkV+v\nv5VrSXv9AgMBAAECggEABm3sl8xgYeH3xtfc1VNLu4ku9Rk5/P1/QJUPAMt6hKM9\nJwLv66QpmwOU4fHity8PHPrB1vtpQ3YDKCKM7UsYJfH+if+WGCN/D7vyB9aiqUBJ\ncjEEvCZ0dq9S8QA7JceecQ8Ev+kmWLMpUnmw3ukeklUrDxg4YFHeBqQBg4or3Pob\nbBHF027MR7CGpyr9o0PlqVCxZiCtfbMF62Hy4KFj6JB3eQ3Js+Z4sXOpSqNHHq+G\n8ywVJBTvVP7j4rbGtuhz7oQx01o927ptDH/Z0WCyO3YDp7sRf8+LIfYnNXAxAiN+\nD5hVd011AIEQuCofI8Fsmf5nstxncMtIjsPm+CN5IQKBgQD2N87O8QGt8zRRNyD5\nQNv1+/1EEkXtzGjiwpNrkR069efCN1i/e+eYtXeXuw4rCjEGULdc+HZvkVFgCKn5\npZ3DwJwwHjEI4WhTka9SmfjxY7CZ9u6kpRZlJ6heRl0qBj4Nqsj/bg1pV3WDrq4\nuUoSDPNxBjdAWwCp/w3Ob+SEbQKBgQDAh9Tr8HIfc1BgnU2tHFGRoz4LzP683Esk\nJ0Djwls24zUFoRAPuFJt2RYKc6Wkw4Ht1bPQRO93yLz7aqJses458M00a8ME3csJ\nkAlft4mpsjpu5sumKAP43jKjs3wzaDmC7+x3PLs7YEo3ZyFy8h80Kt12zTYTkqty\nIHhuRN170QKBgQCaXWLLW04yQMgMIwQJQSCml9WxV8N/0yfhvAw5p4hDxZjpnCUwa\nwRPyKdNQzXWUhk82JmTPZPbb+7+I9eWbHrpKf/dsM4GKj8dYnX3Ny7rHnDicTrRP\nhTEFOlfUwzJCcSE2fQ/PAML83zB1g8aNCZ3mszftJHh/YI6KBd4iDwS2AQKBgQC6\n/7NY7pOJ5JC/JkoZx5WaZPmQsK0Ddtws40ttbIr3xrrrGsLk4dx+AQodYLIUVChQ\nfu5FbY9BwuF7ONlFkAnZ0P8e2UPz6BCa2yGfrD6zaf7DVLucSOWCxR5eTahmreae\nPLZqIbyhMSckpLCiWnTgUHoGN888N4r6MHuIbq7I4QKBgDyKfIoVR7lT/8Fj6a3H\nUkeA5KDRqXkRtorOxOD29GMLdQb8jJNqTRk/v6EQevP74Vumov48tBlWqAbWEJg0\nMnh66GDnI3Cp5DBmfzwM+hBsCctkOiIcNtnA7WXr8pRKFiCOTcVzU+MWBwSiJStx\nC8G8dosnKZRy1DFrbKEMAnkh\n-----END PRIVATE KEY-----\n"
CLIENT_EMAIL="xxxx@eminent-kit-397511.iam.gserviceaccount.com"
CLIENT_ID=103516675153050616893
AUTH_URI=https://accounts.google.com/o/oauth2/auth
TOKEN_URI=https://oauth2.googleapis.com/token
AUTH_PROVIDER_X509_CERT_URL=https://www.googleapis.com/oauth2/v1/certs
CLIENT_X509_CERT_URL=https://www.googleapis.com/robot/v1/metadata/x509/xxxxx%40eminent-kit-397511.iam.gserviceaccount.com
UNIVERSE_DOMAIN=googleapis.com
EMAIL=your_email@email.com
```
4. Миграции для создания базы данных SQLite:
```
* инициализируйте Alembic в проекте `alembic init --template async alembic`
* создайте файла миграции `alembic revision --autogenerate -m "migration name"`
* примените миграций `alembic upgrade head`
* отмена миграций `alembic downgrade`
```
5. Запустите проект:

```
uvicorn app.main:app --reload
```

### Автор проекта:

[Дмитрий Морозов](https://github.com/Esposus "GitHub аккаунт")