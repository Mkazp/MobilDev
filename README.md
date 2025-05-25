1. Клонируйте репозиторий
git clone https://github.com/ВАШ_ЮЗЕРНЕЙМ/ИМЯ_РЕПОЗИТОРИЯ.git
cd ИМЯ_РЕПОЗИТОРИЯ

2. Установите зависимости
Убедитесь, что установлен Node.js и npm:
node -v
npm -v
Затем установите все зависимости:
npm install

3. Настройте переменные окружения
Создайте файл .env в корне проекта (если он не создан) и добавьте туда необходимые переменные. Например:
env
DATABASE_URL="postgresql://user:password@localhost:5432/dbname"
JWT_SECRET="ваш_секретный_ключ"
Переменные зависят от того, как настроено приложение. Смотреть в ConfigModule.forRoot(...) в main.ts.

4. Запустите миграции Prisma (если используется база данных)
npx prisma generate
npx prisma migrate dev

5. Запустите проект в режиме разработки
npm run start:dev

6. Другие команды
npm run build	- Сборка проекта
npm start	- Запуск собранного проекта
npm run format	- Форматирование кода через Prettier
npm run lint	- Линтинг кода с исправлениями
npm run test	- Запуск unit-тестов
npm run test:watch	- Запуск тестов в watch-режиме
npm run test:e2e	- Запуск e2e-тестов
