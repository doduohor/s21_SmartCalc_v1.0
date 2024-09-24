# SmartCalc v1.0

## Описание

SmartCalc v1.0 — это многофункциональный калькулятор, разработанный с использованием стандарта C11 и компилятора GCC. Программа поддерживает вычисление сложных арифметических выражений, включая поддержку вещественных чисел и возможность построения графиков функций. Калькулятор обладает графическим пользовательским интерфейсом, созданным на основе QT, и включает специальный режим "кредитный калькулятор".

## Функционал

- Вычисление арифметических выражений в инфиксной нотации.
- Поддержка целых и вещественных чисел, включая экспоненциальную запись.
- Построение графиков функций с переменной x.
- Кредитный калькулятор с расчетом ежемесячного платежа, переплаты и общей выплаты.

## Технологии

- Язык программирования: C (C11)
- Компилятор: GCC
- GUI-библиотека: Qt
- Тестирование: библиотека Check для unit-тестов
- Стиль кода: Google Style

## Установка

### Зависимости

Убедитесь, что у вас установлены GCC, Make и необходимые GUI-библиотеки.

### Сборка
```
1. Клонируйте репозиторий:
git clone [ссылка на репозиторий]
```
```
2. Перейдите в каталог проекта:
cd [название проекта]/src
```
```
3. Переключитесь на ветку develop:
git switch develop
```
```
4. Запустите сборку проекта:
make
```
### Установка

Для установки выполните:
```
make install
```

## Использование
```
Запустите исполняемый файл из командной строки:
./frontend/build_project/calculate
```

Для использования кредитного калькулятора выберите соответствующий режим в GUI.

## Разработка

### Структура проекта

- `src/backend/` - исходный код программы.
- `src/frontend/` - реализация графического интерфейса 
- `src/backend/tests/` - модульные тесты.
- `src/frontend/build_project/` - директория, в которой собирается проект

### Тестирование

Для запуска unit-тестов используйте:
```
make test
```