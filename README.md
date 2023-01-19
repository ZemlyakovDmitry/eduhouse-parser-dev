# eduhouse-parser-dev
Бот для парса портала Eduhouse

На данный момент официальная стабильная версия бота находится по этому адресу t.me/tkuik_stable_bot

Весь код по сути делится на два слоя: слой для работы с ТГ и низкоуровневые утлиты. 
В низкоуровневых утилитах есть скрипт для скачивания файлов с портала, парса их в специальные объекты и прочее.
Это все находится в ./low_level<br>
./resources представляет собой папку для создания разных подсистем состояний, ORM и прочего. Эти объекты напрямую используются в боте.

Сам код бота находится в bot.py

## Как запустить бота на локальном сервере?
Для начала, необходимо создать виртуальное окружение при помощи утилиты virtualenv:
`virtualenv env`
Далее, активируйте ее при помощи скриптов в директории ./scripts (Зависит от вашей платформы, способы активации на Linux и Windows отличаются)
После этого используя команду `pip install -r requirements.txt` установите необходимые пакеты.
Перед запуском бота необходимо задать 3 переменные окружения:
1. BOT_TOKEN - токен для вашего бота в Telegram, если у вас его нет, можно создать нового с помощью BotFather
2. EDUHOUSE_LOGIN - ваш логин от эдухауса, он вместе с паролем нужен для работы модуля парсинга. Не беспокойтесь, бот нигде не хранит эти данные, и после выключения его на локальном хосте данные будут удалены автоматически.
3. EDUHOUSE_PASSWORD - пароль от эдухауса.

После этого вы можете спокойно менять код и тестировать его на своем компьютере. Если вы сделали какую-либо новую функцию для бота, исправили баг или просто улучшиили код - не стесняйтесь создавать пул-реквесты или открывать issue, если есть какие то проблемы для фикса.

Внимание! Хостинг исходного кода на своем сервере с целью выдачи его за свою работу ЗАПРЕЩЕН!
Исходный код предоставляется всем желающим для поиска багов и уязвимостей, а также помощи в реализации нового функционала.

