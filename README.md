
# Приложение "BAMBARBIA DRIVER" предназначенно для взаимодействия водителя и диспетчера:
# Реализованно
Авторизация при входе в приложение: Проверка данных "Пазывного и пароля" указанных в хранилище файл 
**[CardFileOfDrivers.txt]**

                                    _Вывод: на экран МЕНЮ:_
* 1: `Показать Все Заказы:`
Пункт меню указывает на чтение из файла **[OrderFile.txt]** - далее именуется как "файл заказов", 
Файл с данными о заказах сформированных диспетчером.
* 2: `Показать ближайшие заказы:`
Указывает на чтение из файла заказов тех закозов которые находятся в непосредственной близости к водителю.
* 3: `Показать заказ с наибольшей стоимостью:`
Пункт меню читает из файла заказов ту строку у которой в графе стоимость самая большая стоимость.
* 4: `Показать заказы не дешевле чем...:`
Выводит заказы большие от указанного диапазона.
* 5: `Сортировать по цене от...и до ...:`
Выводит заказы с ценой в диапазоне указзанных водителем.
* 6: `Взять заказ:`
Пункт меню ищет заказ из файла **[OrderFile.txt]** по указанному ID - номеру введенному в консоли,
и обновляет файл **[OrderFile.txt]**, заменяя в заказе поле адресс на пазывной водителя - указанный при входе
в приложение. Данная функция позволяет идентифицировать заказ для передачи его диспетчеру.
Дополнительно реализован функционал записи строки с заказом в новый файл **[Accept.txt]**
добовляя время принятия заказа.
* 7: `Изменить конечный адресс поездки:`
Пункт меню добовляет функционал в консоли приложения для самостоятельной замены адресса при изменении маршрута.
Обновляет файл **[OrderFile.txt]** с изменением поля адресс. Записывает заказ в хранилище **[Accept.txt]**
с обновленной датой.
* 8: `Посмотреть отчет о проделанных заказах:`
Читает из файла **[Accept.txt]** принятые или измененные ранее все заказы.
* 9: `Завершить работу:`
Проверено на возможные ошибки выполнения и ввода/вывода данных.

Структура проекта
de.ait
app - здесь размещается точка входа в приложение (main)
models - модели предметной области
repositories - классы, которые отвечают за получение данных
service - бизнес-логика вашего проекта