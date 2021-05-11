# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

10.05.2021 - 10.05.2021 было проведено функциональное приложения Credit Card Number Validator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* [Карта VISA с номером из 19 цифр отмечается как невалидная](https://github.com/Yu-Smirnova/java-hw-1-part1/issues/1#issue-884900827)
* [Карты American Express (AMEX) отмечаются как невалидные](https://github.com/Yu-Smirnova/java-hw-1-part1/issues/2#issue-884958766)


## Описание процесса тестирования

В качестве тестовых данных использовались данные:
* VISA (номер карты состоит из 16 цифр): 4024007155189235; 4716221120818942; 4929959262444851 ([генератор номеров карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)); ожидаемый результат - OK
* VISA (номер карты состоит из 19 цифр): 4454033003940466519; 4716765769812597237; 4991655785183102037 ([генератор номеров карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)); ожидаемый результат - OK 
* MasterCard: 5126145664281442; 5526372457892922; 2221007614723512 ([генератор номеров карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)); ожидаемый результат - OK
* American Express (AMEX): 349798391358537; 347394348125955; 347275404229411 ([генератор номеров карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)); ожидаемый результат - OK
* Maestro: 6762482363938957; 5018123888760641; 5018657128236789 ([генератор номеров карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)); ожидаемый результат - OK
* Пустое поле; ожидаемый результат - FAIL
* Символы в номере карты (пробел, спецсимволы, буквы); ожидаемый результат - FAIL
* Некорректный номер карты; ожидаемый результат - FAIL
* Номер карты менее 16 цифр; ожидаемый результат - FAIL
* Номер карты более 16 цифр; ожидаемый результат - FAIL

Тестирование производилось в следующем окружении:
* ОС Windows 10, 64-разрядная
* Java 11.0.10
