# Исследование рынка заведений общественного питания Москвы

[Исходный код тетрадки](./catering_market.ipynb)
> [!NOTE]
> Отображение графиков библиотеки plotly можно увидеть только в [html версии тетрадки](https://bussdaria.github.io/portfolio/catering_market/catering_market.html)


Инвесторы из фонда «Shut Up and Take My Money» решили попробовать себя в новой области и открыть заведение общественного питания в Москве. Заказчики ещё не знают, что это будет за место: кафе, ресторан, пиццерия, паб или бар, - и какими будут расположение, меню и цены.
Для начала они просят вас подготовить исследование рынка Москвы, найти интересные особенности и презентовать полученные результаты, которые в будущем помогут в выборе подходящего инвесторам места.


## Данные


В наличии были следующие данные сервисов Яндекс Карты и Яндекс Бизнес на лето 2022 года:
- `name` - название заведения;
- `address` - адрес заведения;
- `category` - категория заведения, например «кафе», «пиццерия» или «кофейня»;
- `hours` - информация о днях и часах работы;
- `lat` - широта географической точки, в которой находится заведение;
- `lng` - долгота географической точки, в которой находится заведение;
- `rating` - рейтинг заведения по оценкам пользователей в Яндекс Картах (высшая оценка - 5.0);
- `price` - категория цен в заведении, например «средние», «ниже среднего», «выше среднего» и так далее;
- `avg_bill` - строка, которая хранит среднюю стоимость заказа в виде диапазона, например:
1. «Средний счёт: 1000–1500 ₽»;
2. «Цена чашки капучино: 130–220 ₽»;
3. «Цена бокала пива: 400–600 ₽» и так далее.
- `middle_avg_bill` - число с оценкой среднего чека, которое указано только для значений из столбца `avg_bill`, начинающихся с подстроки «Средний счёт»:
1. Если в строке указан ценовой диапазон из двух значений, в столбец войдёт медиана этих двух значений.
2. Если в строке указано одно число - цена без диапазона, то в столбец войдёт это число.
3. Если значения нет или оно не начинается с подстроки «Средний счёт», то в столбец ничего не войдёт.
- `middle_coffee_cup` - число с оценкой одной чашки капучино, которое указано только для значений из столбца `avg_bill`, начинающихся с подстроки «Цена одной чашки капучино»:
1. Если в строке указан ценовой диапазон из двух значений, в столбец войдёт медиана этих двух значений.
2. Если в строке указано одно число - цена без диапазона, то в столбец войдёт это число.
3. Если значения нет или оно не начинается с подстроки «Цена одной чашки капучино», то в столбец ничего не войдёт.
- `chain` - число, выраженное 0 или 1, которое показывает, является ли заведение сетевым (для маленьких сетей могут встречаться ошибки):
1. `0` - заведение не является сетевым
2. `1` - заведение является сетевым
- `district` - административный район, в котором находится заведение, например Центральный административный округ;
- `seats` - количество посадочных мест.


## Задача

1. Посчитать количество объектов общественного питания по категориям;
2. Посчитать количество посадочных мест в местах по категориям;
3. Узнать соотношение сетевых и несетевых заведений;
4. Узнать какие категории заведений чаще являются сетевыми;
5. Найти ТОП-15 популярных сетей в Москве;
6. Посчитать общее количество заведений и количество заведений каждой категории по районам;
7. Изучить распределение средних рейтингов по категориям заведений;
8. Найти ТОП-15 улиц по количеству заведений;
9. Найти улицы, на которых находится только один объект общепита;
10. Посчитать средний чек заведений каждого района;
11. Узнать, влияет ли расстояние до центра на средний чек.


## Используемые библиотеки
*pandas, matplotlib, seaborn, plotly, folium, geopy*