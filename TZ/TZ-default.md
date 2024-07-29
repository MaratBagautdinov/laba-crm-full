# Техническое задание

## Цели разработки

### Введение
<p>Разрабатываемая CRM система предназначена для учета клиентов, сделок и продаж компании с целью обеспечить структурированное хранение данных и дальнейший их <b>анализ для выявления слабых и сильных сторон ведения бизнеса компании</b>, оценки эффективности сотрудников, финансовых потоков от тех или иных клиентов компании. </p>
<p>Система должна поддерживать модульность, что позволяло бы в дальнейшем сторонним разработчикам создавать свои компоненты, расширяющие возможности системы. </p>

### Основания для разработки
### Назначение разработки

## Функциональные требования

### Сущности системы

#### Ключевые
* Инициатор и владелец проекта — компания, которая владеет CRM-системой.
    - Наименование
    - Логотип
    - Описание
* Пользователь — это лицо, который зарегистрировано в системе. Его возможности зависят от роли, которую он выполняет: администратор, сотрудник или контрагент.
    - Наименование
    - Пароль
    - Роль
* Контрагент — это человек или организация, которому предоставляется коммерческое "Предложение" в рамках "Сделки". 
    - Наименование
    - Роль
* Сделка — это договор между компанией, которая предоставляет «Предложение», и «Контрагентом». Цель этого «Предложения» — обеспечить определённые услуги или товары. От лица компании в сделке участвует пользователь, который имеет необходимые «Права» для заключения таких договоров. 
    - Менеджер
    - Клиент
    - Торговые предложения
    - Статус
* Предложение — это услуга или товар, которые могут стать предметом потенциальной сделки.
    - Наименование 
    - Цена
    - Единица измерения
    - Валюта

#### Сопутствующие
* Права
    - Наименование
    - Идентификатор
* Роли (типы) пользователей
    - Наименование
    - Права</i>
* Статус сделки 
    - Наименование
    - Цвет
* Валюта
    - Наименование
    - Идентификатор
* Единица измерения
    - Наименование
    - Идентификатор

### Перечень функциональных возможностей системы

- Пользователям системы могут присваиваться набор прав, позволяющие осуществлять следующие действия:
    * Авторизация 

    * Просмотр сделок 
    * Редактирование и создание сделок
    * Удаление сделок

    * Просмотр клиентов 
    * Редактирование и создание клиентов
    * Удаление клиентов

    * Просмотр пользователей системы 
    * Редактирование и создание пользователей
    * Удаление пользователей
### Функциональные блоки

1. Аутентификация
    - процедуры, отвечающие за вход пользователя в систему
2. Авторизация
    - отслеживание прав пользователя
3. Пользователи
    - создание пользователей
    - редактирование пользователей
4. Роль пользователей
    - создание
    - редактирование - назначение списка прав
5. Сделки
    - создание
    - редактирование
    - смена статуса
    - просмотр
6. Клиенты
    - создание
    - редактирование
    - просмотр
7. Настройки системы
    - тема визуального интерфейса
8. Уведомления
    - массовые рассылки клиентам
    - уведомления на почту
    - рассылки в мобильном приложении

### Типы пользователей в системе

1. Гость (анонимный пользователь)
    - Просмотр презентационной страницы
2. Системный администратор
    * Авторизация 

    * Просмотр сделок 
    * Редактирование и создание сделок
    * Удаление сделок

    * Просмотр клиентов 
    * Редактирование и создание клиентов
    * Удаление клиентов

    * Просмотр пользователей системы 
    * Редактирование и создание пользователей
    * Удаление пользователей
3. Сотрудники
    * Авторизация 

    * Просмотр сделок 
    * Редактирование и создание сделок

    * Просмотр клиентов 
    * Редактирование и создание клиентов

    * Просмотр пользователей системы
4. Клиенты
    * Авторизация 
    * Просмотр сделок

### Интерфейсы системы
<b><i> ПРИМЕЧАНИЕ: Пронумерованная строка - страница. Строка с маркером - содержимое страницы </i></b>

#### Презентационная-гостевая страница
Общая информационная страница с описанием ключевых возможностей системы, о способе приобретения, установке
#### Страница входа
Страница ввода логина и пароля для входа в защищенную часть сайта (личный кабинет)

Элементы и блоки:
- Форма ввода логина/пароля
#### Панель управления
<p>Страница со списком возможностей CRM системы</p>

Элементы и блоки:
- Сделки
- Пользователи
- Контрагенты
    1. Сотрудники
        <p>Страница со списком пользователей имеющие роль “Сотрудник”</p>

        Элементы и блоки:
        - Список сотрудников
        1. Детальная страница
            - создание <i>(админ)</i>
            - редактирование <i>(админ)</i>
            - просмотр
        2. Аналитика
            - по занятости
            - тенденция по количеству сделок
            - по иным полям
    2. Контрагенты
        <p>Страница клиентов или организаций</p>
        Элементы и блоки:
        - Список Контрагентов
        1. Детальная страница
            - создание <i>(админ)</i>
            - редактирование <i>(админ)</i>
            - просмотр
        2. Аналитика
            - тенденция по датам
            - тенденция по количеству сделок
            - по иным полям
    3. Сделки
        <p>Страница Сделок</p>

        Элементы и блоки:
        - Список Сделок
        - Фильтр по статусу или иным параметрам
        - Сортировка по параметрам
        1. Детальная страница
            - создание <i>(админ)</i>
            - редактирование <i>(админ)</i>
            - просмотр
        2. Аналитика
            - тенденция по датам
            - по иным полям
    4. Предложения
        <p>Страница Предложения</p>

        Элементы и блоки:
        - Дерево разделов с товарами/услугами
        - Фильтр по параметрам
        - Сортировка по параметрам
        1. Детальная страница
            - создание <i>(админ)</i>
            - редактирование <i>(админ)</i>
            - просмотр
        2. Аналитика
            - по популярности
            - тенденция по совершённым сделок
            - по иным полям
    5. Настройки
        <p>Страница Настройки</p>

        Элементы и блоки:
        - Информация о компании
        - Лого компании
        - Информация о возможностях CRM
        - Настройка ролей и прав
        - Настройка статусов сделок

### Сущности системы

#### Ключевые
* Инициатор и владелец проекта — компания, которая владеет CRM-системой.
    - Наименование
    - Логотип
    - Описание
* Пользователь — это лицо, который зарегистрировано в системе. Его возможности зависят от роли, которую он выполняет: администратор, сотрудник или контрагент.
    - Наименование
    - Пароль
    - Роль <i> (Идентификатор <- "Роли") </i>
* Контрагент — это человек или организация, которому предоставляется коммерческое "Предложение" в рамках "Сделки". 
    - Наименование
    - Роль <i> (Идентификатор <- "Роли") </i>
* Сделка — это договор между компанией, которая предоставляет «Предложение», и «Контрагентом». Цель этого «Предложения» — обеспечить определённые услуги или товары. От лица компании в сделке участвует пользователь, который имеет необходимые «Права» для заключения таких договоров. 
    - Менеджер <i> (Идентификатор <- "Пользователь") </i>
    - Клиент <i> (Идентификатор <- "Клиент") </i>
    - Торговые предложения <i> (Список идентификаторов <- "Предложение") </i>
    - Статус <i> (Идентификатор <- "Статус сделки") </i>
* Предложение — это услуга или товар, которые могут стать предметом потенциальной сделки.
    - Наименование 
    - Цена
    - Единица измерения
    - Валюта

#### Сопутствующие
* Права <i>-> "Роли"</i>
    - Наименование
    - Идентификатор
* Роли (типы) пользователей <i>-> "Пользователь"</i>
    - Наименование
    - Права (список идентификаторов) </i>
* Статус сделки <i>-> "Сделка"</i>
    - Наименование
    - Цвет
* Валюта <i>-> "Предложение"</i>
    - Наименование
    - Идентификатор
* Единица измерения <i>-> "Предложение"</i>
    - Наименование
    - Идентификатор

## Требования к документации

- Необходимо снабдить подробной документацией процесс создания сторонних дополнений к системе
- Необходимо предоставить подробное руководство пользователя в текстовом или видео формате

## Стадии и этапы разработки

### Разработка технического задания
### Разработка диаграммы интерфейсов
### Разработка прототипов интерфейсов
### Разработка дизайн-системы и сборка визуальных макетов интерфейсов
### Программирование серверной логики (backend-разработка)
### Верстка интерфейсов и Frontend-разработка