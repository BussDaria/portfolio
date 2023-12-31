# Исследование оттока клиентов банка "Метанпромбанк"

[Исходный код тетрадки](./bank_customer_outflow.ipynb)
> [!NOTE]
> Отображение графиков библиотеки plotly можно увидеть только в [html версии тетрадки](https://bussdaria.github.io/portfolio/bank_customer_outflow/bank_customer_outflow.html)


Банк "Метанпромбанк" в срочном порядке ищет аналитиков с уверенным владением «Python». Вашей главной задачей станет анализ оттока клиентов. Анализ покажет, какие клиенты уходят из банка, а так же поможет нам составить сегменты клиентов, которые склонны уходить из банка.

Наш заказчик - менеджер из отдела маркетинга, наша общая цель с ним - спасти банк! Привлекать новых клиентов дорого, дешевле удержать тех, про которых мы уже что-то знаем. В нашем отделе маркетинга нету автоматизированных систем рассылок, письма каждому клиенту пишутся вручную, поэтому нам важно для отдела маркетинга представить компактные однородные сегменты и дать примеры мероприятий, которые можно провести, чтобы вернуть клиентов в банк или удержать сомневающихся от оттока.


## Данные

В наличии были следующие данные:
- `USERID` - идентификатор пользователя;
- `score` - баллы кредитного скоринга;
- `city` - город;
- `gender` - пол;
- `age` - возраст;
- `equity` - количество баллов собственности;
- `balance` - баланс на счёте;
- `products` - количество продуктов, которыми пользуется клиент;
- `credit_card` - есть ли кредитная карта;
- `last_activity` - активный клиент;
- `EST_SALARY` - заработная плата клиента;
- `churn` - ушёл или нет.

## Задача

1. Определить, какие факторы влияют на отток клиентов (пол, возраст, город, баллы кредитного скоринга, количество баллов собственности, баланс на счёте, количество продуктов, которыми пользуется клиент, активность клиентов за последнее время, наличие кредитной карты, заработная плата клиентов)
2. Выделить сегменты клиентов, которые склонны уходить из банка.
3. Предложить меры, которые можно провести, чтобы вернуть клиентов в банк или удержать сомневающихся от оттока.


## Используемые библиотеки
*pandas, seaborn, matplotlib, plotly, scipy, phik*