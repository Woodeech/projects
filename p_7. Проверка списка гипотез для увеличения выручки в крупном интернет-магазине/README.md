# Проверка списока гипотез для увеличения выручки в крупном интернет-магазине


## Данные

В наличии были следующие данные:

hypothesis:
- Hypothesis — краткое описание гипотезы;
- Reach — охват пользователей по 10-балльной шкале;
- Impact — влияние на пользователей по 10-балльной шкале;
- Confidence — уверенность в гипотезе по 10-балльной шкале;
- Efforts — затраты ресурсов на проверку гипотезы по 10-балльной шкале. Чем больше значение Efforts, тем дороже проверка гипотезы.

orders:
- transactionId — идентификатор заказа;
- visitorId — идентификатор пользователя, совершившего заказ;
- date — дата, когда был совершён заказ;
- revenue — выручка заказа;
- group — группа A/B-теста, в которую попал заказ.

visitors:
- date — дата;
- group — группа A/B-теста;
- visitors — количество пользователей в указанную дату в указанной группе A/B-теста

## Задача

Используя данные интернет-магазина приоритезировать гипотезы, произвести оценку результатов A/B-тестирования различными методами.  

## Выводы

Гипотезу о том, что различия в конверсиях между группами нет, отвергаем. Относительный прирост конверсии группы `B` равен `17.3%`. По сырым данным относительный прирост конверсии группы `B` равен `13.8%`.

Средний чек группы `B` оказался меньше на `2%` — среднего чека группы `A`. По сырым данным средний чек группы `B` был больше на `25.9%` — среднего чека группы `A`. Если смотреть на очищенные данные, то разницы в среднем чеке между группами `A` и `B` почти нет.

Решение следущее: остановить тест, зафиксировать победу группы `B`, т.к. разница между группами есть, её показатели конверсии выше группы `A`.

## Навыки и инструменты
*Matplotlib*, *SciPy*, *Pandas*, *Datetime*, *A/B-тестирование*, *проверка статистических гипотез*
