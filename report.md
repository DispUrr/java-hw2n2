# Отчёт о тестировании приложения "Precision"
## Краткое описание

- Производилось тестирование процесса пополнения бонусного баланса;
- Оба числа имеют тип *double*;
- При воспроизведении процесса пополнения баланса получаем некорректную итоговую сумму, вероятно, некорректно выбран тип данных.

## Описание тестов

Виды тестирования:
- Функциональное - воспроизводился процесс пополнения баланса;
- Позитивное - использовались строго указанные данные (double regularBonus = 0.3, double specialBonus = 0.6);
- Негативное - меняла тип данных на float (float regularBonus = 0.3f, float specialBonus = 0.6f), так же использовались другие пары цисел: 0.5/0.4 (сумма равна 0.9), 0.2/0.7 (сумма равна 0.8999999999999999), 0.8/0.1 (сумма равна 0.9).

## Результаты

1. 70 % успешных тестов;
1. Ссылки на баг-репорты:
    - [Некорректный рассчет итогового бонуса клиента](https://github.com/DispUrr/java-hw2n2/issues/1)

## Общие рекомендации

Некорректный ответ, вероятнее всего, связан с типом данных.
