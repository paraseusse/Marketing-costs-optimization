# Marketing-costs-optimization
На основе данных о посещениях сайта изучить, как клиенты пользуются продуктом, когда начинают покупать, доход на каждого клиента, окупаемость клиента

Используемые библиотеки: `stats`, `pandas`, `numpy`, `datetime`, `seaborn`, `decimal`

# Задачи
- Анализ пользовательской активности DAU, WAU, MAU
- Когортный анализ
- Расчет LTV и CAC 
- Расчет ROMI

# Выводы

## Выводы по продукту

- В день сервисом в среднем пользуются 907 человек, в неделю: 5716 человек, в месяц: 23228 человек
- В день в среднем проходит 987 сессий, следовательно, на одного пользователя приходится 1.58 сессий
- Есть всплеск активности в декабре и провал в апреле
- Недельная вовлеченность аудитории: 15.8%, месячная вовлеченность аудитории: 3.9%
- Средняя продолжительность сессии до 2 минут
- Более половины сессий длятся менее 5 минут
- Медиана для desktop равняется 6 минутам, для touch вдвое меньше (3)
- Retention низкий, около 5%, и продолжает падать с течением времени 
- Количество покупателей в первых двух когортах почти равны (около 13К), в августе — небольшое снижение, далее начинается рост, достигающий к октябрю-ноябрю почти двукратного увеличения количества пользователей в когорте

### 10% нулевых значений в session_duration_min: либо сессия длилась меньше минуты, либо это случайные клики, либо сбои системы

## Выводы по продажам 

- Среднемесяный чек по когортам равен 7,7 долларов, максимальный = 62,5, минимальный = 2,7
- Средний чек за период равен 4.9
- Первая когорта в лидерах — в среднем участники когорты делают более 3 заказов в месяц
- На одного покупателя в среднем приходится 1.85 покупок 
- Среднее время продолжительности сессии по оформлению заказа — 4 минуты. Ресурс используют только для покупки билетов
- Медианная разница во времени между первым визитом и моментом совершения заказа — 16 минут
- Накопительный LTV одного пользователя в среднем составляет 4 доллара
- Сессии с desktop длятся дольше, чем с touch
- Порядка 75% сессий  — с desktop
- Доход с одного покупателя: 7.23 для desktop, 5.57 для touch, ltv — 3.62 и 2.78 соответсвенно

### Обращаем внимание на несколько аномальных когорт — 4 (сентябрьская) и 7 (декабрьская). По ним средний чек после 2-3 первых месяцев значительно превышал средний чек, возможно, у услуги есть сезонность или были другие влияющие факторы.

## Выводы по маркетингу 
- Всего истрачено 329 131 долларов, заработано 252 057. Бизнес работатет в убыток.
- Каналы
    - 1, 2, 5, 9 каналы окупают себя
    - у 1 канала перспективное соотношение стоимости привлечения и выручки, однако, невысокое соотношение конвертации постетителей в покупатели 
    - 3, 4, 10 каналы не окупают себя
    - 3 рекламный канал наиболее затратный, и он не является лидером по выручке
    - 4 канал дает наибольшую выручку, однако он так же невыгоден, так как затраты превышают выручку
    - 3 и 4 канал лидирует по количеству  привлеченых покупателей

- Чтобы вложения окупались стоимость привлечения одного покупателя не должно превышать 3.9 долларов
- Ни один из каналов не проходит в это горлышко, средние затраты на привлечение одиного покупателя составляют 6.7 долларов 
- На данный момент ни одна из когот не окупилась

# Рекомендации
- Обратить внимание на первую когорту, её Retention rate выше, чем у остальных, ее участники совершают, в среднем, больше покупок
- В период с октября 2017 по март 2018 двукратное увеличение количества посетителей, значит, рекламная кампания работает, как минимум, на привлечение посетителей на сайт, соответственно, необходимо сосредоточить маркетинговые усилия на конверсию посетителя в покупателя и удержание клиента
- Необходимо перераспределить вложения в рекламные каналы и сместить акцент с 3, убыточного для компании канала на каналы 1 и 5
- По 2, 3 и 4 каналам необходимо провести дополнительные исследования и выяснить причины низкой конверсии в покупателя 
- 73% визитов с персонального компьютера, 27% — с мобильных устройств. Рекомендован тест юзабилити мобильной версии сайта и, возможно, создание мобильного приложения
- ROMI при коэффициенте маржинальности в 0.5 ни по одной когорте не добрался до зеленой зоны (значение > 1). Бизнес убыточен
- Стоимость привлечения одного покупателя не должно превышать 3.9 долларов, на данный момент средние затраты на привлечение одиного покупателя составляют 6.7 долларов
