# 🚀 Поиск ликвидных облигаций на Московской Бирже и их анализ

Этот репозиторий содержит три Python-скрипта, которые помогают частным инвесторам находить ликвидные облигации, анализировать денежные потоки и отслеживать новости эмитентов. 

Несмотря на обилие публичных сервисов для поиска облигаций, данное решение выделяется тем, что это open source решение, которое:
1. Формирует краткий список привлекательных вариантов, доступных для покупки прямо сейчас.
2. Проводит анализ денежных потоков.
3. Собирает актуальные новости по каждой компании.

## 🔧 Три отдельных скрипта

### 1️⃣ Поиск ликвидных облигаций
Скрипт взаимодействует с API Московской биржи и фильтрует облигации по важным параметрам. 
На рынке торгуется более 2500 облигаций, но многие из них неликвидны: по ним либо нет предложений, либо их очень мало, что делает покупку невозможной. Этот скрипт отбирает только те облигации, которые действительно доступны для торговли.

~~Читать подробнее об этом скрипте на: [Хабр](https://habr.com/ru/users/empenoso/) | [Смартлаб](https://smart-lab.ru/mobile/users/empenoso/blog/)~~

### 2️⃣ Автоматический расчет денежных потоков
Этот скрипт загружает данные о купонах и выплатах номинала для списка облигаций из Excel-файла, используя API Московской биржи, и записывает результат в отдельную вкладку того же файла. Третья вкладка содержит анализ выплат. Это удобный инструмент для автоматизированного расчета кэшфлоу по облигациям.

Читать подробнее об этом скрипте на: [Хабр](https://habr.com/ru/users/empenoso/) | [Смартлаб](https://smart-lab.ru/mobile/users/empenoso/blog/)

### 3️⃣ Сбор новостей по эмитентам
Используя уже собранные коды ценных бумаг для облигаций на Московской биржи, скрипт получает название эмитента с биржи и затем собирает последние новости по компании. Просмотр заголовков помогает быстро понять, что сейчас происходит с эмитентом и чем он занимается.

~~Читать подробнее об этом скрипте на: [Хабр](https://habr.com/ru/users/empenoso/) | [Смартлаб](https://smart-lab.ru/mobile/users/empenoso/blog/)~~

## 📊 Почему это важно?
Многие частные инвесторы не ведут учет облигационного портфеля, что затрудняет принятие стратегических и тактических решений. Доступные портфельные трекеры платные, а самостоятельное ведение Excel-документов требует значительных усилий. Данный проект создан для тех, кто хочет вести учет облигаций в Excel, но хочет избавиться от рутины.

## 🛠️ Почему Python, а не встроенный Python в Excel?
Я выбрал отдельные скрипты на Python вместо встроенных функций Python в Excel, потому что:
- Встроенный Python работает только в Microsoft Office 2024 и требует подписки Office 365.
- Он поддерживает только ограниченный список библиотек от Microsoft и Anaconda.
- Работает исключительно под Windows.

Скрипты, представленные здесь, лишены этих ограничений и могут использоваться на любой платформе: Windows, MacOS и даже Linux.

## 📂 Установка и запуск
### 1️⃣ Установка зависимостей
Убедитесь, что у вас установлен Python 3.9+ и выполните команду:
```bash
pip install -r requirements.txt
```

### 2️⃣ Запуск скриптов
Найдите скрипты в проводнике и дважды кликните по нужному Вам. Это запустит скрипт, и он обновит или создаст файл Excel. 

После окончания работы можно посмотреть логи работы - скрипт ждёт нажатия кнопки.

```bash
1_bonds_search by criteria.py
2_bonds_search coupons.py
3_bonds_news search_beta.py
```

## 🏆 Альтернативные версии
Если вы хотите использовать JavaScript-версию, у меня есть другой репозиторий с:
- Node.js-версией поиска
- Поиском в Google Таблицах на Google Apps Script

[Смотреть здесь](https://github.com/empenoso/SilverFir-Investment-Report)

## 🤝 Контакты и поддержка
Если у вас есть вопросы или предложения, создавайте issue или pull request. Буду рад обратной связи! 🚀

Автор: Михаил Шардин  
[🔗 Моя онлайн-визитка](https://shardin.name/?utm_source=github)  
[📢 Telegram «Умный Дом Инвестора»](https://t.me/+asaEcPax8o41MjQy)
