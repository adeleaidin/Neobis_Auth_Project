Neobis Auth Project

Проект на Django с JWT, DRF и Celery для аутентификации пользователей.

Функционал

Регистрация и вход по JWT
Подтверждение email через Celery + Redis
Восстановление пароля
API на DRF
Установка и запуск

1. Клонирование проекта
git clone https://github.com/adeleaidin/Neobis_Auth_Project.git
cd Neobis_Auth_Project
2. Виртуальное окружение
python -m venv venv
source venv/bin/activate  # Mac/Linux  
venv\Scripts\activate     # Windows
3. Установка зависимостей
pip install -r requirements.txt
4. Конфигурация
Создайте .env и добавьте:

DB_NAME=your_db_name  
DB_USER=your_db_user  
DB_PASSWORD=your_db_password  
DB_HOST=localhost  
DB_PORT=5432  
SECRET_KEY=your_secret_key  

5. Миграции
python manage.py migrate

6. Запуск сервера
python manage.py runserver
API: http://127.0.0.1:8000/api/
Swagger: http://127.0.0.1:8000/swagger/

7. Запуск Celery
celery -A config worker --loglevel=info

API Эндпоинты

Метод	Эндпоинт	Описание
POST	/api/register/	Регистрация
POST	/api/login/	Вход (JWT)
POST	/api/logout/	Выход
POST	/api/reset-password/	Восстановление пароля
GET	/api/profile/	Данные пользователя


TODO

 OAuth (Google, GitHub)
 Тесты
 Деплой
