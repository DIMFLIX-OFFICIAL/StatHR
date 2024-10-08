
<img src="./docs/logo.png"/>

***

**VisionHire** — интуитивно понятная панель управления для рекрутеров, которая упрощает процесс подбора персонала. Мы предоставляем удобные инструменты для визуализации данных и анализа эффективности, чтобы вы могли делать обоснованные решения и улучшать процесс найма. Отслеживайте ключевые метрики, настраивайте уведомления и интегрируйтесь с популярными платформами — все в одном месте. Ваш успех в подборе начинается здесь.

> [!WARNING]
> **Проект не завершён!** \
> Наша команда не успела завершить проект в назначенный срок. \
> В связи с этим мотивация доделывать проект пропала. \
> На данный момент проект имеет статус заброшенного...

## Проблематика
Рекрутеры часто сталкиваются с трудностями в анализе своей работы и эффективности подбора персонала. 
Существующие инструменты либо слишком сложны в использовании, либо не предоставляют достаточной информации для принятия обоснованных решений. 
Необходим инструмент, который позволит легко отслеживать и анализировать ключевые метрики и действия рекрутера, улучшая процесс подбора персонала.

## Стек
Backend python:  
- `fastapi` - серверная часть
- `sqlalchemy` + `asyncpg` (postgresql) - бд
- `pydantic` - валидация данных
- `aiosmtplib` - уведомления для пользователей
Frontend: 
- `Vue` + `JavaScript` + `SCSS` - основной стек
- `amCharts` - Отрисовка графиков через JS  (есть интеграция с Vue)

# Как пользоваться?
- ## Настройка переменнных окружения 
	1.Создайте файл с переменными окружения `cp .env.example .env` \
	2. Откройте файл .env в любом удобном для Вас текстовом редакторе. \
	3. Обязательно заполните поля:
	- `JWT_TOKEN_SECRET` - токен для шифрования
	- `DB_USERNAME` - логин от базы данных PostgreSQL
	- `DB_PASSWORD` - пароль от базы данных PostgreSQL
	- `SMTP_HOST` - адрес SMTP-сервера
	- `SMTP_PORT` - порт SMTP-сервера
	- `EMAIL` - почта
	- `EMAIL_PASSWORD` - пароль от почты
	- `ADMIN_LOGIN` - логин админа 
	- `ADMIN_PASSWORD` - пароль админа 

- ## Установка зависимостей и запуск
	- ### Backend
		1. [Установите poetry](./docs/POETRY_INSTALL.md)
		2. Перейдите в каталог `backend` с помощью команды `cd backend`
		3. Выполните установку зависимостей `python -m poetry install`
		4. Войдите в виртуальное окружение `python -m poetry shell`
		5. Инициализируйте базу данных `python src/app.py --action=init_db`
		6. Запустите бекенд `python src/app.py` 
	- ### Frontend
		1. Перейдите в каталог `frontend` с помощью команды `cd frontend`
		2. Установите зависимости `npm install`
		3. Запустите сервер `npm run serve`
- ## Управление данными
	С помощью данных, указанных в `ADMIN_LOGIN` и `ADMIN_PASSWORD` вы можете управлять всеми хранящимися данными с помощью удобной админ панели. 
	Для того чтобы её открыть - перейдите по адресу `<ссылка_на_сайт>/admin` и введите данные для входа.

# Разработка
- ## Заполнение данными
	Вы можете заполнить таблицы тестовыми данными. \
	Для этого перейдите в папку `backend/src`
	Далее выполните команду `python app.py --action=fake_fill`

# Вклад в развитие
Вклад в развитие VisionHire приветствуется! \
Если вы обнаружите какие-либо проблемы или у вас есть идеи по улучшению, не стесняйтесь открывать проблему или отправлять запрос на слияние.

# Лицензия
VisionHire распространяется под лицензией MIT. \
Подробнее смотрите в файле [LICENSE](LICENSE).
