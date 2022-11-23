# Задача Магазин

## Описание
Это финальная задача! В этом задании попрактикуемся с правилами чистого кода и принципами SOLID.

Нужно написать программу-магазин, в которой пользователи заказывают товары. Вам предоставляется свобода в продумывании функциональности вашей программы, как и в проектировании её структуры. В процессе реализации вы должны применить принцип избегания магических чисел, DRY и как минимум 4 из 5 принципов SOLID, причём явно комментариями в коде или при отправке решения указать по одному примеру применения каждого принципа в вашем решении со ссылками на конкретные места кода на гитхабе.

Примеры возможностей программы:
* Вывод доступных для покупки товаров
* Фильтрация товаров по ключевым словам, ценам, производителям
* Составление продуктовой корзины пользователя
* Трекинг заказа в системе доставки
* Возврат заказа, повтороение заказа
* Система рейтинга для товаров
* Простая рекомендательная система для покупок

## Реализация
1. Продумайте и зафиксируйте список возможностей вашей программы.
2. Продумайте консольный интерфейс взаимодействия пользователя с вашей программой.
3. Продумайте систему классов, которые вам понадобятся для реализации вашей программы.
4. Напишите вашу программу, явно применив вышеперечисленные принципы хорошего кода.
5. При отправке решения укажите, в чём именно было применение каждого этого принципа (по одному примеру) со ссылками на конкретные места кода на гитхабе.
6. Протестируйте работу программы. Не забывайте про правила форматирования кода (для автоформата можете выделить код в идее и нажать **Ctrl+Alt+L**).

# Решение
Замечания.
1. Класс Purchase нарушает принцип единственной ответственности (single responsiblity principle), являясь одновременно покупкой и корзиной. 
   Необходимо разделить их на два класса.
2. Указание размера массива при инициализации. Для ухода от этого надо передавать
     мапу товаров и цен в конструктор.
   ![img.png](img.png)

Объявим массив в поле без инициализации, инициализируем в конструкторе.

   ![img_3.png](img_3.png)

Класс Main изменим с учетом разделения класса Purchase на Purchase и Basket.
