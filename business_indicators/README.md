# Исследование бизнес показателей развлекательного приложения Procrastinate Pro+

Вы - маркетинговый аналитик развлекательного приложения Procrastinate Pro+. Несмотря на огромные вложения в рекламу, последние несколько месяцев компания терпит убытки. Ваша задача - разобраться в причинах и помочь компании выйти в плюс.


## Данные

Есть данные о пользователях, привлечённых с 1 мая по 27 октября 2019 года:

1) лог сервера с данными об их посещениях:
- `User Id` - уникальный идентификатор пользователя;
- `Region` - страна пользователя;
- `Device` - тип устройства пользователя;
- `Channel` - идентификатор источника перехода;
- `Session Start` - дата и время начала сессии;
- `Session End` - дата и время окончания сессии.


2) выгрузка их покупок за этот период:
- `User Id` - уникальный идентификатор пользователя;
- `Event Dt` - дата и время покупки;
- `Revenue` - сумма заказа.

3) рекламные расходы:
- `dt` - дата проведения рекламной кампании;
- `Channel` - идентификатор рекламного источника;
- `costs` - расходы на эту кампанию.


## Задача

1. Изучить откуда приходят пользователи и какими устройствами они пользуются;
2. Сколько стоит привлечение пользователей из различных рекламных каналов;
3. Сколько денег приносит каждый клиент;
4. Когда расходы на привлечение клиента окупаются;
5. Какие факторы мешают привлечению клиентов.

## Используемые библиотеки
*pandas, seaborn, numpy, matplotlib, datetime*