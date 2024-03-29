# Домашнее задание к занятию "`Работа с данными (DDL/DML)`" - `Аблогин Павел`

---

### Задание 1

1. `Поднял чистый инстанс MySQL версии 8.0.35`
2. `Создал учётную запись sys_temp и дал все права для этого пользователя.`
3. `Переподключился к базе данных от имени sys_temp`
4. `Скачал и восстановил дамп БД.`

```
#SQL-запросы для выполнения задания 1

CREATE USER 'sys_temp'@'%' IDENTIFIED BY 'sys_temp';

use mysql;

select host, user from user;

GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'%' WITH GRANT OPTION;

select * from information_schema.user_privileges where grantee like "'sys_temp'%";

ALTER USER 'sys_temp'@'%' IDENTIFIED WITH mysql_native_password BY 'sys_temp';

use sakila;

show tables;

```

`Скриншоты выполнения задания 1`
![Создание пользователя и список пользователей](img/task1_1.png)
![Выадача прав пользователю и проверка прав](img/task1_2.png)
![Список таблиц восстановленной БД](img/task1_3.png)


---

### Задание 2

```
Результат выполнения задания 2: список таблиц БД и первичных ключей этих таблиц.


+---------------+--------------+
| TABLE_NAME    | PRIMARY_KEY  |
+---------------+--------------+
| actor         | actor_id     |
| address       | address_id   |
| category      | category_id  |
| city          | city_id      |
| country       | country_id   |
| customer      | customer_id  |
| film          | film_id      |
| film_actor    | actor_id     |
| film_actor    | film_id      |
| film_category | film_id      |
| film_category | category_id  |
| film_text     | film_id      |
| inventory     | inventory_id |
| language      | language_id  |
| payment       | payment_id   |
| rental        | rental_id    |
| staff         | staff_id     |
| store         | store_id     |
+---------------+--------------+
 

```

---


