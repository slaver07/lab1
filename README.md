# Лабораторная работа №1: "Алгебра полиномов"

## Техническое задание

### 1. Цель проекта

Разработка программной системы для выполнения алгебраических операций над полиномами от трех переменных (x, y, z) с поддержкой хранения данных в шести различных структурах данных.

----------

### 2. Функциональные требования

#### 2.1 Хранение полиномов

-   Каждый полином хранится  **во всех таблицах одновременно**.
    
-   **Ключ**  для доступа: имя полинома (строка).
    
-   Поддерживаемые структуры данных:
    
    -  Линейная таблица на массиве
        
    -  Линейная таблица на списке
        
    -  Упорядоченная таблица на массиве
        
    -  Дерево (АВЛ или красно-черное)
        
    -  Хеш-таблица с открытой адресацией
        
    -  Хеш-таблица методом цепочек
        

#### 2.2 Операции над полиномами

-   **Для одного полинома**:
    
    -   Вычисление значения в точке (x, y, z).
        
    -   Умножение на константу.
        
    -   Вычисление производной по заданной переменной.
        
    -   Вычисление неопределенного интеграла по заданной переменной.
        
-   **Для выражений из полиномов**  (постфиксная запись):
    
    -   Сложение (+), вычитание (-).
        
    -   Умножение на константу (*).
        
    -   Умножение полиномов (*).
        
    -   Деление полиномов (/).
        

#### 2.3 Операции над таблицами

-   Добавление полинома  **во все таблицы**.
    
-   Удаление полинома  **из всех таблиц**.
    
-   Поиск полинома  **только в активной таблице**  (используется при вычислении выражений).
    
-   Вывод активной таблицы в формате:
    
| Имя полинома | Строковое представление  |
|-------------|------------------------|
| pol1        | 3.2x²y³z - 1.3xz⁴      |

    

#### 2.4 Пользовательский интерфейс

-   Возможность выбора активной таблицы.
    
-   Ввод выражений для вычисления новых полиномов.
    
-   Вывод ошибок при отсутствии полиномов или некорректных операциях.
    

----------

### 3. Пример работы

**Исходные данные в таблицах**:
```
pol1 = 3.2x²y³z - 1.3xz⁴  
pol2 = -3.2x²y³z + 1.3xz⁴  
const6 = 6.0  
q = 4.0x²
```
**Ввод выражения**:  
```
new_pol = 2 * pol1 + 2 * pol2 + 3.6 * q - const6
```
**Результат**:

-   Вычисленный полином: new_pol = 14.4x² - 6.0.
    
-   Полином new_pol добавлен во все таблицы.
    

----------

### 4. Нефункциональные требования

-   Язык реализации: C++.
    
-   Модульная архитектура с четким разделением компонентов:
    
    -   Логика полиномов.
        
    -   Реализация структур данных.
        
    -   Парсер постфиксных выражений.
        
-   Наличие модульных тестов для всех компонентов.
    
-   Документация в формате README.md с примерами использования.
    
----------


### 6. Распределение работ

| Ответственный         | Задача                                      |
|-----------------------|--------------------------------------------|
| **Байков Илья**       | Интерфейс, линейная таблица на массиве, таблица на поисковом дереве (АВЛ/КЧ) |
| **Валентин Кутергин** | Полином, линейная таблица на списке, хеш-таблица с открытым перемешиванием |
| **Вячеслав Долов**    | Постфикс для полиномов, упорядоченная таблица на массиве, хеш-таблица со списками (метод цепочек) |


----------

### 6. План разработки

| Неделя  | Задачи                             |
|---------|------------------------------------|
| 1       | Подготовка ТЗ, создание репозитория |
| 2-3     | Разработка структуры данных       |
| 4-5     | Реализация основных операций      |
| 6       | Разработка интерфейса             |
| 7       | Тестирование                      |
| 8       | Итоговая проверка, сдача проекта  |

----------

### 7. Требования к тестированию

-   Покрытие тестами всех операций над полиномами:
    
    -   Корректность арифметических операций.
        
    -   Проверка вычисления производной/интеграла.
        
-   Тестирование всех типов таблиц:
    
    -   Добавление/удаление.
        
    -   Поиск в активной таблице.
        
-   Проверка обработки ошибок:
    
    -   Несуществующие полиномы в выражениях.
        
    -   Некорректный синтаксис.
        

----------

### 8. Сдача проекта

-   Исходный код в репозитории GitHub.
    
-   Документация (README.md) с инструкцией по запуску.
    
-   Примеры работы программы.
    
-   Отчет о тестировании.
