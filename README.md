### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### Решение  

*1. Сотрудники*

* Идентификатор, первичный ключ, serial
* Фамилия, varchar(50)
* Имя, varchar(50)
* Отчетство, varchar(50)
* Дата найма, date
* Должность, внешний ключ, position_id
* Адрес филиала, внешний ключ, branch_id
* Подразделение, внешний ключ, strdiv_id
* Оклад, внешний ключ, salary_id
* Проект, внешний ключ, project_id

*2. Должность*  

* Идентификатор, position_id, первичный ключ, serial
* Должность, varchar (75)

*3. Тип подразделения*  

* Идентификатор, division_id, первичный ключ, serial
* Тип, varchar (75)

*4. Структурное подразделение*  

* Идентификатор, strdiv_id, первичный ключ, serial
* Подразделение, varchar (75)
* division_id, внешний ключ, integer

*5. Адрес филиала*  

* Идентификатор, branch_id, первичный ключ, serial
* Адрес, varchar (255)

*6. Проект*  

* Идентификатор project_id, первичный ключ, serial
* Проект, varchar (75)

*7. Оклад*  

* Идентификатор salary_id, первичный ключ, serial
* Оклад, decimal (9,2)

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.


### Задание 2*

Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.
