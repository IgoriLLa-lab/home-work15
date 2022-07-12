# home-work15

Домашнее задание
1. Выбрать всех сотрудников с серией паспорта 1015 и номером 422269
Решение:
SELECT * FROM `workers` WHERE series = 422269 AND number = 1015;
![image](https://user-images.githubusercontent.com/67729776/178448006-e6629d06-4cb2-49d7-8b63-d63e49139a34.png)

2. Найти всех сотрудников с именем Алексей c датой рождения после 1 июля 1999
года
Решение:
SELECT * FROM `workers` WHERE first_name = 'Алексей' AND birthday > '1999-07-01';
![image](https://user-images.githubusercontent.com/67729776/178448130-7dab01cc-efcb-4f48-9c35-c9632810df02.png)

3. Подсчитать какое количество сотрудников работает в компании 'Cеверсталь'
Решение:
SELECT COUNT(*) AS "Кол-во сотрудникво Северстали" FROM `workers` WHERE company = 'Северсталь';
![image](https://user-images.githubusercontent.com/67729776/178448245-da2b3ba6-d7c3-4c64-8b54-012bb3fd536b.png)

4. Выбрать всех инженеров с датой рождения между 1 декабря 1979 и 1 февраля
1980, отсортированных по имени и фамилии
Решения:
SELECT * FROM `workers` 
WHERE role = 'Инженер' 
AND birthday >= '1979-12-01' AND birthday <= '1980-02-01' 
ORDER BY first_name ASC, last_name ASC;
![image](https://user-images.githubusercontent.com/67729776/178448783-1cb00fa5-9c73-493c-8295-95fc962098df.png)

2й вариант

SELECT * FROM `workers` 
WHERE role = 'Инженер' 
AND birthday BETWEEN '1979-12-01' AND '1980-02-01' 
ORDER BY first_name ASC, last_name ASC;
![image](https://user-images.githubusercontent.com/67729776/178448859-64b1fc8a-7de2-469c-b66a-465e2b34a483.png)

5. Выбрать всех сотрудников с должностями Химик-технолог, Химик и Биохимик,
которые работают в X5 Retail Group отсортированных по дате рождения - от
молодых к старым
Решение:

SELECT * FROM `workers` 
WHERE role IN ('Химик-технолог', 'Химик', 'Биохимик')
AND company = 'X5 Retail Group'
ORDER BY birthday DESC;
![image](https://user-images.githubusercontent.com/67729776/178448921-2ac602fe-55cb-47c2-8982-db2bf8833dc8.png)

Тестовая база данных для задания располагается по ссылке:
https://disk.yandex.ru/d/LBDa38UjGrFA6Q
