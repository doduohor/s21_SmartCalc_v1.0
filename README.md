# SmartCalc v1.0

## Введение

**SmartCalc v1.0** — это многофункциональный калькулятор, разработанный с использованием стандарта C11 и компилятора GCC. Программа предназначена для вычисления сложных арифметических выражений, поддерживает работу с вещественными числами, а также предоставляет возможность построения графиков функций. Калькулятор оснащён графическим пользовательским интерфейсом, созданным на основе Qt, и включает специализированный режим "Кредитный калькулятор" для расчёта кредитных платежей.

## Цели и задачи проекта

### Цели

- Разработка надежного и удобного калькулятора для вычисления арифметических выражений.
- Обеспечение расширенных функциональных возможностей, таких как построение графиков и кредитные расчёты.
- Соблюдение высоких стандартов качества кода и тестирования.

### Задачи

- Реализация парсинга и вычисления арифметических выражений с учетом приоритетов операций и скобок.
- Разработка графического интерфейса пользователя с использованием Qt.
- Внедрение функционала построения графиков функций.
- Создание модуля "Кредитный калькулятор" для расчёта ежемесячных платежей и общей переплаты.
- Обеспечение покрытия кода unit-тестами с использованием библиотеки Check.
- Настройка системы сборки с помощью Makefile.

## Описание проекта

**SmartCalc v1.0** представляет собой калькулятор, который выходит за рамки базовых возможностей стандартных приложений. Он поддерживает не только базовые арифметические операции, но и сложные математические функции, работу с переменными и построение графиков. Дополнительно, калькулятор оснащён режимом "Кредитный калькулятор", который позволяет пользователям рассчитывать ежемесячные платежи, общую переплату и итоговую сумму по кредиту.

## Функциональные возможности

### Вычисление арифметических выражений

- **Парсинг выражений:**
  - Реализован лексический и синтаксический анализатор для разбора вводимых арифметических выражений.
  - Используется алгоритм преобразования инфиксной нотации в обратную польскую (ОПН) для учёта приоритетов операций и скобок.

- **Поддерживаемые операции:**
  - **Арифметические операторы:**
    - Сложение (`+`)
    - Вычитание (`-`)
    - Умножение (`*`)
    - Деление (`/`)
    - Возведение в степень (`^`)
    - Остаток от деления (`mod`)
    - Унарные операции (`+a`, `-a`)
  
  - **Математические функции:**
    - Синус (`sin(x)`)
    - Косинус (`cos(x)`)
    - Тангенс (`tan(x)`)
    - Арксинус (`asin(x)`)
    - Арккосинус (`acos(x)`)
    - Арктангенс (`atan(x)`)
    - Квадратный корень (`sqrt(x)`)
    - Натуральный логарифм (`ln(x)`)
    - Десятичный логарифм (`log(x)`)

- **Переменная x:**
  - Возможность подстановки значения переменной `x` в выражения.
  - Позволяет пользователю задавать значение `x` для вычисления функций и построения графиков.

### Построение графиков функций

- **Графический интерфейс:**
  - Интеграция с Qt обеспечивает интуитивно понятный и удобный интерфейс.
  
- **Функциональные возможности:**
  - Ввод математических функций с переменной `x`.
  - Автоматическое построение графиков с координатными осями, адаптивной сеткой и отметками масштаба.
  - Ограничение области определения и области значений функций от -1,000,000 до 1,000,000.
  - Отображение ключевых точек функции, таких как пересечения с осями.

- **Техническая реализация:**
  - Использование Qt Charts для визуализации графиков.
  - Обработка ошибок ввода и отображение уведомлений пользователю в случае некорректных выражений.

### Кредитный калькулятор

- **Функционал:**
  - **Входные данные:**
    - **Сумма кредита:** Общая сумма займа.
    - **Срок кредита:** Продолжительность кредита в месяцах или годах.
    - **Процентная ставка:** Годовая процентная ставка.
    - **Тип кредита:** Выбор между аннуитетным и дифференцированным платежом.
  
  - **Выходные данные:**
    - **Ежемесячный платеж:** Размер ежемесячного платежа.
    - **Переплата по кредиту:** Общая сумма переплаты за весь срок кредита.
    - **Общая выплата:** Сумма кредита плюс переплата.
  
- **Техническая реализация:**
  - Реализация алгоритмов расчета аннуитетных и дифференцированных платежей.
  - Валидация вводимых данных и обработка возможных ошибок (например, отрицательные значения).

## Технологии и инструменты

- **Язык программирования:** C (C11)
- **Компилятор:** GCC
- **GUI-библиотека:** Qt
- **Тестирование:** Библиотека [Check](https://libcheck.github.io/check/)
- **Стиль кода:** [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
- **Система сборки:** Makefile
- **Система контроля версий:** Git

## Архитектура системы

Архитектура **SmartCalc v1.0** основана на модульном подходе, что обеспечивает удобство разработки, тестирования и поддержки проекта.

### Основные модули

1. **Backend:**
    - **Парсер выражений:** Отвечает за разбор и преобразование вводимых арифметических выражений.
    - **Вычислитель:** Выполняет вычисления на основе разобранных выражений.
    - **Модуль графиков:** Обрабатывает данные для построения графиков функций.
    - **Кредитный калькулятор:** Реализует алгоритмы расчёта кредитных платежей.

2. **Frontend:**
    - **GUI:** Обеспечивает взаимодействие с пользователем, отображение результатов и управление режимами калькулятора.
    - **Модули взаимодействия:** Обеспечивают связь между пользовательским интерфейсом и backend-модулями.

3. **Тестирование:**
    - **Unit-тесты:** Покрывают функциональные модули backend, обеспечивая их корректную работу.


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
