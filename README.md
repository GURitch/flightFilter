#Тестовое задание по созданию фильтров для перелетов

В ветке dev находится реализация, выполненная в виде отдельных методов класса FlightFilterImpl с использованием stream().
Добавлен метод валидации, при этом возможна излишняя итерация по коллекции сегментов. Но учитывая что сегментов в одном перелете не может быть очень много, это не должно влиять на производительность.

Также в репозитории имеется Pull Request с альтернативной реализацией через отдельные классы.
Там используются циклы for, операторы if и каждая проверка на возможные ошибки производится не отдельно, а непосредственно в теле метода, что позитивно отразиться на производительности при работе с большими коллекциями объектов.
Методы могут выглядеть усложненными, возмона разбивка функционала на более мелкие и узкоспециализированные методы.
Класс FlightFilterChain создается на основе нескольких классов-фильтров, тем самым позводляет выполнить фильтрацию коллекции перелетов сразу по нескольким параметрам